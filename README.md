[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/Deltares/CanOpenFEWS/pulls)

# CanOpenFEWS

Open and shareable configuration for an operational hydrological forecasting system with [Delft-FEWS](https://oss.deltares.nl/web/delft-fews).

A complete system configuration is provided for data access, processing, visualization and application in hydrological modelling. The technical focus is on rain and snow for operational forecasting, and applied in a mountainous environment. The data sources are primarily [Meteorological Service of Canada Open Data](https://eccc-msc.github.io/open-data/readme_en/).

This repository has been made to spur community development, so please feel free to use the configuration in your own applications.

Also make contributions back! Whether new data, models, methods or displays are all welcome.


## Rainfall Nowcasting

** Put description and images of Nowcasting

## Snow Monitoring

CanOpenFEWS contains bindings to a variety of snow data products, and aims to connect measurement to modelling for snowmelt driven streamflow forecasting. The use of snow data within the system remains largely qualitative, also comparison of multiple products such as [Snowcast](http://www.snowcast.ca/), [SNODAS](https://nsidc.org/data/g02158/versions/1), [GlobSnow](https://www.globsnow.info/) and [in-situ observations](https://rivers.alberta.ca/). This suite of products will be expanded, and in consultation with end-users, methods added to connect snow measurement to model.

![SnowDisplayExample](SnowGIF.gif)

## Hydrological Models

CanOpenFEWS currently contains two hydrological models over the Bow Basin in Alberta, Canada. The two models (both open source) are included to demonstrate connections to a distributed (grid-based) and semi-distributed (vector based) conceptual model. Both models contain a variety of options for discretizations, and conceptual process representation.

Both are flexible hydrological modelling frameworks, with supporting tools for model creation, implementation and evaluation.

### wflow

[wflow](https://deltares.github.io/Wflow.jl/stable/) allows multiple distributed model concepts are available, allowing the use of open earth observation data, making it the hydrological model of choice for data scarce environments. Based on gridded topography, soil, land use and climate data, wflow calculates all hydrological fluxes at any given grid cell in the model at a given time step. Creation of wflow models is enabled by the [HydroMT](https://deltares.github.io/hydromt/latest/) python package


### Raven Hydrological Framework


[Raven](http://raven.uwaterloo.ca/) is flexible hydrological modelling framework, allowing flexibility in spatial discretization, interpolation, process representation, and forcing function generation. In this repository, a semi-distributed HBC-EC concept model is implemented to demonstrate the model bindings and connections.

TODO: Add description

## Getting Started

Instructions for getting started with CanOpenFEWS configuration is available here (TODO). Please contact also Dave Casson and Ruben Imhoff for more information.

## Collaborators

This configuration is the collaboration of researchers, engineers and end-users.

Deltares (the Netherlands), Deltares USA, Dave Casson (SWFTResponse / University of Calgary) and several Canadian partners and Delft-FEWS users (TODO: fill in this list).

Special thanks for the Alberta River Forecast Center and to the City of Calgary Water Resources department for feedback and contributions. Also to Rob Chlumsky of [Heron Hydrologic] (https://heronhydrologic.ca/) for providing the base Raven model and description.

## License

CanOpenFEWS is licensed under an MIT license, which generally is quite open and permissive. Please see the LICENSE file for details.

## How to contribute?
TO DO

## Citations

National Operational Hydrologic Remote Sensing Center. (2004). Snow Data Assimilation System (SNODAS) Data Products at NSIDC, Version 1 [Data Set]. Boulder, Colorado USA. National Snow and Ice Data Center. https://doi.org/10.7265/N5TB14TC. Date Accessed 12-08-2023.
