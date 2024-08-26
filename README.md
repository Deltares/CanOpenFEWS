[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/Deltares/NextOpenFEWS/pulls)

# NextOpenFEWS

NextOpenFEWS is an open and shareable configuration for an operational hydrological forecasting system with [Delft-FEWS](https://oss.deltares.nl/web/delft-fews). This repository is meant to share developments and receive input from the forecasting community. It is experimental and demonstration only.


The workflows allow data access and processing for a number of public data sources in Canada and the US. Primary data sources are the [NOAA Operational Model Archive and Distribution System (NOMADS)](https://nomads.ncep.noaa.gov/) [Meteorological Service of Canada Open Data](https://eccc-msc.github.io/open-data/readme_en/), but also include a variety of snow and meterological re-analysis products, such as ERA5.

This repo is intended for those with some experience with the Delft-FEWS software. It is hosted on GitHub so that users can access workflows, model connections and displays for their own use. Please feel free to use the configuration to develop and improve your own applications. Also make contributions back! New data, methods, models and displays are all welcome.


## Hydrological Models

NextOpenFEWS currently contains hydrological modelling frameworks over the Yukon River Basin, a transboundary basin across the Yukon and Alaska. 

### SUMMA

[SUMMA](https://ral.ucar.edu/model/summa) or the Structure for Unifying Multiple Modeling Alternatives is a hydrologic modeling approach that is built on a common set of conservation equations and a common numerical solver, which together constitute the structural core of the model.

SUMMA can be used to configure a wide range of hydrological model alternatives. Different modeling approaches can then be implemented within the structural core, enabling a controlled and systematic analysis of alternative modeling options, and providing insight for future model development. SUMMA allows different model representations of physical processes and spatial configurations to be flexibly implemented and tested.
Creation of SUMMA models is enabled by the well documented [CWARHM](https://github.com/CH-Earth/CWARHM) workflow. This provides all tools necessary to build SUMMA models from scratch.

In NextOpenFEWS, a SUMMA model is implemented for the Bow River basin, using a semi-distributed Hydrological Response Unit approach to better represent the spatial distribution of snow and other variables.

## Getting Started

If you are truly new to this software, it may be better to begin with the information [available on the Delft-FEWS website](https://oss.deltares.nl/web/delft-fews). At this link, you can find the latest information, instructions and community developments. Configuring Delft-FEWS comes with a steep learning curve, but once you are familiar with it, this repository can help to minimize reinventing the wheel by sharing configuration and it is a great way to test and share new developments (models, code, etc.).

### Installation of Delft-FEWS

Download and installation instructions are available [at this webpage, at the bottom](https://oss.deltares.nl/web/delft-fews/about-delft-fews). Delft-FEWS is free to use, but please note that a end-user license agreement is required. For further detail on obtaining Delft-FEWS, including new releases, please contact [fews-pm email](fews-pm@deltares.nl). The newest Delft-FEWS versions are only available through [fews-pm email](fews-pm@deltares.nl), but older versions can be directly downloaded from the website. This configuration has been tested with the v2023.01 of Delft-FEWS. It is possible that some functionalities do not work with other (older) versions of Delft-FEWS.

Please note that Delft-FEWS runs on Windows and Linux, and is not normally run on Mac OS.

### Using the NextOpenFEWS configuration

A complete functioning configuration is available on this GitHub repository. 

If you do not plan on contributing back to the repository, it can simply be downloaded from the main page. If you do plan on contributing, which is very welcome, you will need to use git, or a program like GitHub Desktop.

## License

NextOpenFEWS is licensed under an MIT license, which generally is quite open and permissive. Please see the LICENSE file for details.

## How to contribute?
Contributions to NextOpenFEWS are much appreciated. However, to ensure continuity and a stable code base, we ask you to do the following when you plan to contribute with changes, new config or new models:

*(1) Fork the repository*

*(2) Create a new branch*

All contributions should be made in a new branch under your forked repository. Working on the master branch is reserved for Core Contributors only. Core Contributors are developers that actively work and maintain the repository. They are the only ones who accept pull requests and push commits directly to the pysteps repository.For more information on how to create and work with branches, see [Branches in a Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) in the Git documentation.

*(3) Create a pull request based on the changes in your branch*

The pull requests are checked by the main contributors and merged with the main repository once accepted.

## Citations

### Delft-FEWS
Werner, M., Schellekens, J., Gijsbers, P., van Dijk, M., van den Akker, O., and Heynert, K. (2013). The Delft-FEWS flow forecasting system. *Environ Modell Softw*, 40, 65–77. doi: [10.1016/j.envsoft.2012.07.010](https://doi.org/10.1016/j.envsoft.2012.07.010).

### SUMMA

Clark, M. P., B. Nijssen, J. Lundquist, D. Kavetski, D. Rupp, R. Woods, E. Gutmann, A. Wood, L. Brekke, J. Arnold, D. Gochis, and R. Rasmussen, 2015a: A unified approach to process-based hydrologic modeling. Part 1: Modeling concept. Water Resources Research, 51, doi: [10.1002/2015WR017198](https://doi.org/10.1002/2015WR017198)

Clark, M. P., B. Nijssen, J. Lundquist, D. Kavetski, D. Rupp, R. Woods, E. Gutmann, A. Wood, D. Gochis, R. Rasmussen, D. Tarboton, V. Mahat, G. Flerchinger, and D. Marks, 2015b: A unified approach for process-based hydrologic modeling: Part 2. Model implementation and example applications. Water Resources Research, 51, doi: [10.1002/2015WR017200](https://doi.org/10.1002/2015WR017200)

Knoben, W. J. M., Clark, M. P., Bales, J., Bennett, A., Gharari, S., Marsh, C. B., et al. (2022). Community Workflows to Advance Reproducibility in Hydrologic Modeling: Separating model-agnostic and model-specific configuration steps in applications of large-domain hydrologic models. Water Resources Research, 58, e2021WR031753. doi: [10.1029/2021WR031753](https://doi.org/10.1029/2021WR031753)
