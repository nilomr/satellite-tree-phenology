
![Title Badge](https://img.shields.io/badge/phenosat-k?style=for-the-badge&labelColor=d99c2b&color=d99c2b) ![R Badge](https://img.shields.io/badge/v4.2-4295B3?style=for-the-badge&logo=r&logoColor=white)



## Table of Contents

- [Table of Contents](#table-of-contents)
- [This Repository](#this-repository)
  - [Project Organization](#project-organization)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Dependencies](#dependencies)
- [Running the analyses](#running-the-analyses)
  - [Models](#models)
  - [Figures and model output](#figures-and-model-output)
- [Bugs and Issues](#bugs-and-issues)



## This Repository

This repository includes the following main features,

- An RStudio project [`phenosat.Rproj`](./phenosat.Rproj)
- Package dependency management using [`renv`](https://github.com/rstudio/renv/)
- Configuration using [`config`](https://github.com/rstudio/config)
- A [`scripts`](./scripts) directory with the code necessary to reproduce the analysis and figures in this paper.
- A [`R`](./R) folder for R source code and reusable functions


### Project Organization

```text
.
├── data
│   ├── derived
│   │   └── satellite
│   │       └── quadrant_1
│   │           ├── 2001
│   │           └── 2002
│   ├── metadata
│   └── raw
│       ├── satellite
│       │   └── quadrant_1
│       └── shapefiles

```

## Getting Started


### Installation

Clone this repository to your local computer using the following command in the terminal:
  
```bash
git clone https://github.com/nilomr/satellite-tree-phenology.git
```

 - [] TODO: Then, download the data from [OSF](), replacing the `data` folder in the repository with the downloaded `data` folder[^1].


### Dependencies

This project uses R v4.2. You must have the [`renv` package](https://rstudio.github.io/renv/articles/renv.html) installed on your local computer. While in an active session, simply run the following line of code in the R Console.

```r
install.packages('renv')
```

To install the necessary libraries using `renv`, run the following line of code in the R Console:

```r
renv::restore()
```
Depending on your system, this may take a while, and you will likely be prompted (as in installation will just fail) to install some system dependencies.


## TODO

  - [x] Rename quadrant folders to remove capital letters and whitespaces
  - [ ] Make explicit the variable name equivalences:

```r

variable_equivalences <- c(
    "Dormancy" = "Onset_Dormancy",
    "Amplitude" = "EVI_Amplitude",
    "Area" = "EVI_Area",
    "Minimum" = "Minimum_EVI",
    "Greenup" = "Onset_Greenness_Increase",
    "Maturity" = "Onset_Maturity",
    "MidGreendown" = "Middle_Greenness_Decrease",
    "MidGreenup" = "Middle_Greenness_Increase",
    "Peak" = "Date_of_Peak",
    "Senescence" = "Onset_Greenness_Decrease"
)

```

## Bugs and Issues

If you encounter any bugs or issues, please [open an issue](https://github.com/nilomr/birdsong-demography/issues/new/choose). If possible, include a minimal reproducible example and/or screenshots to illustrate the problem.


<br>

[^1]: Data are under version control here, but obtaining these requires `git-lfs` to be installed on your computer and I can't guarantee that it will work.

<sub>
<br>© Nilo M. Recalde, 2023
</sub>

