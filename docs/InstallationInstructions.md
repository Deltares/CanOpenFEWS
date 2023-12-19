# Installation instruction for CanOpenFEWS
## Getting Started

If you are truly new to this software, it may be better to begin with the information [available on the Delft-FEWS website](https://oss.deltares.nl/web/delft-fews). At this link, you can find the latest information, instructions and community developments. Configuring Delft-FEWS comes with a steep learning curve, but once you are familiar with it, this repository can help to minimize reinventing the wheel by sharing configuration and it is a great way to test and share new developments (models, code, etc.).

## Installation of Delft-FEWS

Download and installation instructions of Delft-FEWS are available [at this webpage, at the bottom](https://oss.deltares.nl/web/delft-fews/about-delft-fews). Delft-FEWS is free to use, but please note that a end-user license agreement is required. For further detail on obtaining Delft-FEWS, including new releases, please contact fews-pm@deltares.nl. The newest Delft-FEWS versions are only available through fews-pm@deltares.nl, but older versions can be directly downloaded from the website. This configuration has been tested with the v2023.01 of Delft-FEWS. It is possible that some functionalities do not work with other (older) versions of Delft-FEWS.

Please note that Delft-FEWS runs on Windows and Linux, and is not normally run on Mac OS.

## Using the CanOpenFEWS configuration

The fully functioning CanOpenFEWS configuration can be downloaded from this GitHub repository. If you do not plan on contributing back to the repository, it can simply be downloaded from the main page. If you do plan on contributing, which is very welcome, you will need to use git, or a program like GitHub Desktop, to clone the repository into your own environment.

After cloning the repository to your own computer, make sure to make a so-called Delft-FEWS shortcut through `/[Loc_fews_distribution]/bin/[operator_system]/createShortcuts.exe]`, which places a `CanOpenFEWS.lnk` in your CanOpenFEWS folder. With this link, you can launch the CanOpenFEWS Delft-FEWS. The Delft-FEWS createShortcuts functionality will open the display in the figure below. Point to `/clientConfig.xml` in the CanOpenFEWS folder and the link will be automatically created. 

![createShortcuts_example](docs/Delft-FEWS_Shortcuts.png)


### External modules
Several external modules are used in CanOpenFEWS. Many of these modules are already present in the ModuleDataSetFiles (/Config/ModuleDataSetFiles) of the configuration and will be automatically found by the configuration upon launching Delft-FEWS and/or the specific workflow that calls them in a model run. However, the distribution of Python (with all modules and pysteps already installed), R (with all packages installed) and wflow are too large to store on github. Instead, we have stored these distributions elsewhere. If you are planning to use them to download ECCC data, run wflow, run pysteps, etc., then you can download these distributions at the following locations: [Python and R](https://zenodo.org/doi/10.5281/zenodo.10369454), and [wflow](https://download.deltares.nl/en/wflow). Make sure to unpack the zip files in the `/Modules` folder under the folder names: Python311 (for Python), R-4.1.1 (for R) and wflow_cli (for wflow). These module names can be changed, but in case you decide to do so, make sure to change the executable directory names in `/sa_global.properties` as well.


## NetCDF installation

https://docs.unidata.ucar.edu/netcdf-c/current/winbin.html
