![wide logo](https://user-images.githubusercontent.com/44177991/194967300-52177111-5c48-4012-8051-44319c14f914.png)
## What is this?
This organisation contains the imperial third year group project work under the supervision of [Dr Nicolas Wu](https://www.imperial.ac.uk/people/n.wu) and constitued by:
- Jordan Hall
- Bartłomiej Cieślar
- Robbie Buxton
- Ethan Range
- Charlie Lidbury
- Oliver Killane

## Project Origin
1. Auto Labelling is a crucial part of supervised machine learning.
2. FusedEffects provides the ability to embed domain specific languages within Haskell
3. The ProbFX library is a DSL for probabilistic programming, developed using FusedEffects

## Project Aims
To use and if necessary extend ProbFX to generate basic auto labelling for features such as road markings.

- Image Manipulation library (using FusedEffects).
- Model creation using ProbFX to demonstrate its potential.
- Model refinement using MCMC and othet techniques.
- To develop an mvp for lane labelling using the above.

## Relevant Resources
### Fused Effects
A library to enable embedded DSL creation within Haskell. 

[Hackage](https://hackage.haskell.org/package/fused-effects) | [GitHub](https://github.com/fused-effects/fused-effects)

### ProbFX
A probabilistic programming DSL embedded within haskell as a library.

[Paper](https://github.com/min-nguyen/prob-fx/raw/main/paper.pdf) | [GitHub](https://github.com/min-nguyen/prob-fx)

### CULane
A dataset of images of lanes to be labelled by our models.

[Website](https://xingangpan.github.io/projects/CULane.html)

### Gen-LaneNet
3D lane line generation from images.

[GitHub - Pytorch Implementation](https://github.com/yuliangguo/Pytorch_Generalized_3D_Lane_Detection) | [Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123660664.pdf)

### Approximate Bayesian Image Interpretation using Generative Probabilistic Graphics Programs
Details a similar approach to that which we are taking.

[Paper](https://arxiv.org/pdf/1307.0060.pdf)


## Reports
### Team Agreement
Our first report detailing how we intend to work, basic plan for the project and potential risks.

[Report](https://github.com/Functional-Labelling-Lab/.github/blob/master/reports/Team%20Agreement/Team_Agreement.pdf)


## Git Hygiene
### Branch Naming Convention
```bash
prefix/branch-name-here
```

| Prefix | Description                                                                               |
|--------|-------------------------------------------------------------------------------------------|
| enh    | An enhancement (e.g new feature, or improving an existing feature)                        |
| ref    | Refactor - should not change behaviour                                                    |
| fix    | Fixing a bug, the jira ticket should be included - branch name can be generated from jira |
| doc    | Adding or amending documentation                                                          |
| msc    | Miscellaneous, any other change                                                           |

### Pull Requests
This [pull request template](./../pull_request_template.md) is used for all repos.
- Description
- Goals of PR (for reviewer to compare with the achieved)
- Current changes and intended changes (in case of draft PR)
