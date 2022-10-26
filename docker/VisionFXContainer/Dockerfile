FROM haskell:8.10.7-buster AS base

# Update repositories
RUN apt-get update -y
RUN cabal update

# Install OpenCV
FROM base AS opencv
RUN apt-get install -y cmake g++ wget unzip libgtk2.0-dev pkg-config

RUN mkdir /opencv-build
WORKDIR /opencv-build

ADD https://github.com/opencv/opencv/archive/3.4.16.zip opencv.zip
RUN unzip opencv.zip

RUN mkdir build
WORKDIR /opencv-build/build
RUN cmake ../opencv-3.4.16

RUN cmake --build .

RUN make install

# Build Cabal dependencies
FROM opencv AS dependencies

# Language Server Support
RUN cabal install haskell-language-server

# Set up paths to access OpenCV libs
ENV INCLUDE_PATH=$HOME/usr/include:${INCLUDE_PATH}
ENV LD_LIBRARY_PATH=$HOME/usr/local/lib:${LD_LIBRARY_PATH}

RUN mkdir /code
WORKDIR /code

COPY *.cabal cabal.project ./

RUN cabal build --only-dependencies -j4 all

ENTRYPOINT ["/bin/bash"]