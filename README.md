[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/Deltares/CanOpenFEWS/pulls)

# CanOpenFEWS

CanOpenFEWS is an open and shareable configuration for an operational hydrological forecasting system with [Delft-FEWS](https://oss.deltares.nl/web/delft-fews).

This repository is meant to share developments and receive input from the forecasting community. It contains complete examples for data access, processing, visualization and application in hydrological modelling.

The technical focus is on rainfall nowcasting and snow monitoring for operational forecasting, applied in a mountainous environment. The data sources are primarily [Meteorological Service of Canada Open Data](https://eccc-msc.github.io/open-data/readme_en/), but include a variety of remote sensing and re-analysis products.

Please feel free to use the configuration to develop and improve your own applications. Also make contributions back! New data, methods, models and displays are all welcome.


## Rainfall Nowcasting

CanOpenFEWS contains a rainfall nowcasting module that uses the open source nowcasting platform [pysteps](https://pysteps.readthedocs.io/en/latest/). With nowcasting, the most recent rainfall observations are extrapolated to the future using optical flow methods (for advection) and statistical methods (for rainfall growth/dissipation estimation and post-processing purposes). The advantage of nowcasting is that it should provide more accurate rainfall forecasts for the first hours into the future than rainfall forecasts from numerical weather prediction models. Generally observations from weather radar are used for nowcasting, as weather radar provides a good spatial coverage, and high spatial and temporal resolution. This is advantageous for an observation-based forecasting technique such as nowcasting. In CanOpenFEWS, the ECCC radar product is used for nowcasting. 

Pysteps contains a variety of nowcasting models and in CanOpenFEWS the models [STEPS](https://pysteps.readthedocs.io/en/latest/auto_examples/plot_steps_nowcast.html#sphx-glr-auto-examples-plot-steps-nowcast-py) and [LINDA](https://pysteps.readthedocs.io/en/latest/auto_examples/linda_nowcasts.html#sphx-glr-auto-examples-linda-nowcasts-py) are conigured. Both models can be run in a deterministic and an ensemble setup. The gif below shows an example of one ensemble member of an ensemble STEPS forecast (left) and a deterministic run with the LINDA model (right) for December 18, 2023. The LINDA model is generally regarded as the better option for convective rainfall, but it has slower run times than the STEPS model. CanOpenFEWS contains the ECCC radar imports, the nowcast model runs (the number of ensemble members can be set in the properties of the configured workflows), viewers of the radar and nwocasts data and the option to use the nowcast output as input for the hydrological model runs. At a later stage, a blending procedure can also be added to CanOpenFEWS. 

![NowcastingDisplayExample](docs/gif_nowcast_20231218.gif)


## Snow Monitoring

CanOpenFEWS contains bindings to a variety of snow data products, and aims to connect measurement to modelling for snowmelt driven streamflow forecasting. The use of snow data within the system remains largely qualitative, also comparison of multiple products such as [Snowcast](http://www.snowcast.ca/), [SNODAS](https://nsidc.org/data/g02158/versions/1), [GlobSnow](https://www.globsnow.info/) and [in-situ observations](https://rivers.alberta.ca/). This suite of products will be expanded, and in consultation with end-users, methods added to connect snow measurement to model.

![SnowDisplayExample](docs/SnowGIF.gif)

## Hydrological Models

CanOpenFEWS currently contains two hydrological models over the Bow Basin in Alberta, Canada. The two models (both open source) are included to demonstrate connections to a distributed (grid-based) and semi-distributed (vector based) conceptual model. Both models contain a variety of options for discretizations, and conceptual process representation.

Both are flexible hydrological modelling frameworks, with supporting tools for model creation, implementation and evaluation.

### wflow

[wflow](https://deltares.github.io/Wflow.jl/stable/) allows multiple distributed model concepts are available, allowing the use of open earth observation data, making it the hydrological model of choice for data scarce environments. Based on gridded topography, soil, land use and climate data, wflow calculates all hydrological fluxes at any given grid cell in the model at a given time step. Creation of wflow models is enabled by the [HydroMT](https://deltares.github.io/hydromt/latest/) python package

### Raven Hydrological Framework


[Raven](http://raven.uwaterloo.ca/) is flexible hydrological modelling framework, allowing flexibility in spatial discretization, interpolation, process representation, and forcing function generation. In this repository, a semi-distributed HBV-EC concept model is implemented to demonstrate the model bindings and connections.

This repository is intended for those with some experience with the Delft-FEWS software.
It is hosted on GitHub so that users can access workflows, model connections and displays for their own use.



## Getting Started

If you are truly new to this software, it may be better to begin with the information [available on the Delft-FEWS website](https://oss.deltares.nl/web/delft-fews). At this link, you can find the latest information, instructions and community developments.

### Installation of Delft-FEWS

Download and installation instructions are available [at this webpage, at the bottom](https://oss.deltares.nl/web/delft-fews/about-delft-fews). Please note that a end-user license agreement is required. For further detail on obtaining Delft-FEWS, including new releases, please contact fews-pm@deltares.nl

Please note that Delft-FEWS runs on Windows and Linux, and is not normally run on Mac OS.

### Using the CanOpenFEWS configuration

A complete functioning configuration is available on this GitHub repository.

If you don't plan on contributing back to the repository, it can simply be downloaded from the main page. If you do plan on contributing, which is very welcome, you will need to use git, or a program like GitHub Desktop.

TO DO: Expand

### Collaborators
TO DO: Clean this section up

This configuration is the collaboration of researchers, engineers and end-users.


Deltares (the Netherlands), Deltares USA, Dave Casson (SWFTResponse / University of Calgary) and several Canadian partners and Delft-FEWS users (TODO: fill in this list).

Special thanks for the Alberta River Forecast Center and to the City of Calgary Water Resources department for feedback and contributions. Also to Rob Chlumsky of [Heron Hydrologic](https://heronhydrologic.ca/) for providing the base Raven model and description.

## License

CanOpenFEWS is licensed under an MIT license, which generally is quite open and permissive. Please see the LICENSE file for details.

## How to contribute?
TO DO

## Citations

### Delft-FEWS
Werner, M., Schellekens, J., Gijsbers, P., van Dijk, M., van den Akker, O., and Heynert, K. (2013). The Delft-FEWS flow forecasting system. *Environ Modell Softw*, 40, 65–77. doi: `10.1016/j.envsoft.2012.07.010 <https://doi.org/10.1016/j.envsoft.2012.07.010>`_.

### Nowcasting
The overall pysteps library is described in:

Pulkkinen, S., D. Nerini, A. Perez Hortal, C. Velasco-Forero, U. Germann, A. Seed, and L. Foresti (2019). Pysteps: an open-source Python library for probabilistic precipitation nowcasting (v1.0). *Geosci. Model Dev.*, 12 (10), 4185–4219, doi:`10.5194/gmd-12-4185-2019 <https://doi.org/10.5194/gmd-12-4185-2019>`_.

While the more recent blending module in pysteps is described in:

Imhoff, R.O., L. De Cruz, W. Dewettinck, C.C. Brauer, R. Uijlenhoet, K-J. van Heeringen, 
C. Velasco-Forero, D. Nerini, M. Van Ginderachter, and A.H. Weerts (2023). Scale-dependent blending of ensemble rainfall nowcasts and NWP in the open-source pysteps library. *Q J R Meteorol Soc.*, 1-30, doi: `10.1002/qj.4461 <https://doi.org/10.1002/qj.4461>`_.

The STEPS method is described in:

Bowler, N.E., Pierce, C.E., and Seed, A.W. (2006). STEPS: A probabilistic precipitation forecasting scheme which merges an extrapolation nowcast with downscaled NWP. *Q J R Meteorol Soc.*, 132(620), 2127–2155, doi: `10.1256/qj.04.100 <https://doi.org/10.1256/qj.04.100>`_.

The LINDA method is described in:
Pulkkinen, S., Chandrasekar, V., and Niemi, T. (2021). Lagrangian Integro-Difference Equation Model for Precipitation Nowcasting. *J Atmos Ocean Tech*, 38(12), 2125-2145, doi: `10.1175/JTECH-D-21-0013.1 <https://doi.org/10.1175/JTECH-D-21-0013.1>`_.

### Snow data
National Operational Hydrologic Remote Sensing Center (2004). Snow Data Assimilation System (SNODAS) Data Products at NSIDC, Version 1 [Data Set]. Boulder, Colorado USA. National Snow and Ice Data Center. https://doi.org/10.7265/N5TB14TC. Date Accessed 12-08-2023.
