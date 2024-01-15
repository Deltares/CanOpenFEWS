# How to Access Password Protected Data

## Introduction

The CanOpenFEWS relies on public data sources, however several of the data sources are password protected.
A description of how to get data access is provided below:
- [Radar Data from ECCC MSC DataMart](#radar_data)
- [National Surface and River Prediction System from ECCC MSC GeoMet](#nsrps_data)
- [ERA5 Reanalysis Data from the Copernicus Data Store](#nsrps_data)

## Radar Data

Composite radar data is available as an experimental data set from [Environment Canada and Climate Change DataMart](https://eccc-msc.github.io/open-data/msc-datamart/readme_en/).

Steps to access the data are:

  1. Contact dps-client@ec.gc.ca for password specific to this product

  2. Add the username and password to the global.properties file

## NSRPS Data

National Surface and River Prediction System is available as an experimental data set from [Environment Canada and Climate Change GeoMet Services](https://eccc-msc.github.io/open-data/msc-geomet/readme_en/).

  1. Contact dps-client@ec.gc.ca for password specific to this product

  2. Add the username and password to the global.properties file


## ERA5 Data

Noting first that only new credentials and creation of a .cdsapirc file are needed. ERA5 data can be accessed from the Copernicus Climate Data Store.

  1.  Accessing credentials for ERA5 data following instructions on  Copernicus website [here](https://cds.climate.copernicus.eu/api-how-to).

  2. In the case of Windows installation, add the .cdsapirc to the Modules/pyscripts/bin directory.
