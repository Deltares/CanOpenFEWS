# Installation instruction for CanOpenFEWS
## Getting Started

If you are truly new to this software, it may be better to begin with the information [available on the Delft-FEWS website](https://oss.deltares.nl/web/delft-fews). At this link, you can find the latest information, instructions and community developments. Configuring Delft-FEWS comes with a steep learning curve, but once you are familiar with it, this repository can help to minimize reinventing the wheel by sharing configuration and it is a great way to test and share new developments (models, code, etc.).

## Pulling the repository to your own environment

The first time you are using CanOpenFEWS, you will have to pull the contents of the repository to your own computer environment. Go the folder where you want the CanOpenFEWS folder to end up and either download and unpack the CanOpenFEWS zip file in this folder or type in a (git) command line:

`git clone https://github.com/Deltares/CanOpenFEWS.git`

Now, you are ready to go. Every time you plan to work on and make changes to the repository, make sure to first update your CanOpenFEWS to the latest version of the repository. In a (git) command line, navigate to the CanOpenFEWS folder and type:

`git fetch`

followed by:

`git pull`

You are up to date now and ready to make changes and commit them. Contributing to CanOpenFEWS is explained in [How to contribute?](https://github.com/Deltares/CanOpenFEWS).

## Installation of Delft-FEWS

Download and installation instructions of Delft-FEWS are available [at this webpage, at the bottom](https://oss.deltares.nl/web/delft-fews/about-delft-fews). Delft-FEWS is free to use, but please note that a end-user license agreement is required. For further detail on obtaining Delft-FEWS, including new releases, please contact [fews-pm email](fews-pm@deltares.nl). The newest Delft-FEWS versions are only available through [fews-pm email](fews-pm@deltares.nl), but older versions can be directly downloaded from the website. This configuration has been tested with the v2023.01 of Delft-FEWS. It is possible that some functionalities do not work with other (older) versions of Delft-FEWS.

Please note that Delft-FEWS runs on Windows and Linux, and is not normally run on Mac OS.

## Using the CanOpenFEWS configuration

The fully functioning CanOpenFEWS configuration can be downloaded from this GitHub repository. If you do not plan on contributing back to the repository, it can simply be downloaded from the main page. If you do plan on contributing, which is very welcome, you will need to use git, or a program like GitHub Desktop, to clone the repository into your own environment.

After cloning the repository to your own computer, make sure to make a so-called Delft-FEWS shortcut through `/[Loc_fews_distribution]/bin/[operator_system]/createShortcuts.exe]`, which places a `CanOpenFEWS.lnk` in your CanOpenFEWS folder. With this link, you can launch the CanOpenFEWS Delft-FEWS. The Delft-FEWS createShortcuts functionality will open the display in the figure below. Point to `/clientConfig.xml` in the CanOpenFEWS folder and the link will be automatically created. 

![createShortcuts_example](/docs/Delft-FEWS_Shortcuts.png)


### External modules
Several external modules are used in CanOpenFEWS. Many of these modules are already present in the ModuleDataSetFiles (/Config/ModuleDataSetFiles) of the configuration and will be automatically found by the configuration upon launching Delft-FEWS and/or the specific workflow that calls them in a model run. However, the distribution of Python (with all modules and pysteps already installed), R (with all packages installed), JCEF (for web viewers) and wflow are too large to store on github. Instead, we have stored these distributions elsewhere. If you are planning to use them to download ECCC data, run wflow, run pysteps, etc., then you can download these distributions at the following locations: [Python and R](https://zenodo.org/doi/10.5281/zenodo.10369454), and [wflow](https://download.deltares.nl/en/wflow). Make sure to unpack the zip files in the `/Modules` folder under the folder names: Python311 (for Python), R-4.1.1 (for R) and wflow_cli (for wflow). These module names can be changed, but in case you decide to do so, make sure to change the executable directory names in `/sa_global.properties` as well. In addition, the JCEF zip file can be downloaded on the [FEWS wiki page](https://publicwiki.deltares.nl/display/FEWSDOC/24+Web+Browser+Display). Make sure to put the zip file in the `./Config/ModuleDataSetFiles` folder and uncomment the automatic export of this zip file in the `clientConfig.xml` of the main folder.


## NetCDF installation

https://docs.unidata.ucar.edu/netcdf-c/current/winbin.html
