# NOTES

## Scope

What is the scope of the tutorial? Here's some suggestions:

 - Nomenclature
    + PROJ, proj?
    + Operations, conversions, projections & transformations
    + Coordinate systems, datums, reference frames, coordinate reference systems
    + ISO19111?
 - Core concepts of transformations in PROJ
    + projstrings
    + ellipsoids
    + cartographic projections
    + helmert transform
    + pipelines
 - The command line utilities
    + projinfo
    + proj
    + cct
    + cs2cs

## Presentations

* [Introduction](https://docs.google.com/presentation/d/1sEFspKT4xUUWm9gCdLoNYd1OLJcMxxFW4cf7HELD3JM/edit?usp=sharing)

* [Practical exercises](https://docs.google.com/presentation/d/1V0eCxJvzRg8s2sJ0WoTs6ZDcWUbmQgA9VX5KlEWp60M/edit?usp=sharing)


## Program

*Preliminary schedule - subject to changes*

- 12:00 - 13:00   Lunch
- 13:00 - 13:45   Introduction to PROJ, Kristian Evers
- 13:45 - 14:15   ETRS89 Transformations in Fennoscandia, Pasi Häkli
- 14:15 - 14:45   Dynamic reference frame in Iceland, Gudmundur Valsson
- 14:45 - 15:15   Coffee break
- ????? - ?????   ???
- 16:00 - 1800    Practical exercises, Kristian Evers

## Installation

We will be using the `conda` command line system to install and run PROJ
in. In short, `conda` let's you install and update various command line
tools in an easy way. You need the following two files to get started:

* [Miniconda Windows 64-bit](https://repo.continuum.io/miniconda/Miniconda2-4.5.12-Windows-x86_64.exe)
* [PROJ Windows 64-bit](https://anaconda.org/conda-forge/proj4/6.0.0/download/win-64/proj4-6.0.0-ha7a8c7b_0.tar.bz2)

Save them somewhere on your computer where you can find them. For simplicity,
this guide downloads them to the root of the C-drive: `C:\`.

In case your are not installing this on Windows, you need to download the correct
installers for your system. Find the Miniconda installer [here](https://repo.continuum.io/miniconda/) and the PROJ package [here](https://anaconda.org/conda-forge/proj4/6.0.0/download/win-64/proj4-6.0.0-ha7a8c7b_0.tar.bz2). The installation steps below will
also be different but the overall workflow is the same. Chances are you can
work things out by yourself (it's not that complicated).

Installation steps:

1. Run the installer
2. When asked, select "Just Me" (the default option)
3. The default installation folder is fine, continue
4. Finish the installation

After the installation is done open the "Anaconda Prompt" from the Windows start menu.
When the prompt is open, enter the command

    conda install C:\proj4-6.0.0-ha7a8c7b_0.tar.bz2

Wait a bit until the installation is finished. Once the installation is over you can try
issueing a PROJ command:

    projinfo ETRS89

which should result in output similar to:

    PROJ.4 string:
    +proj=longlat +ellps=GRS80 +towgs84=0,0,0,0,0,0,0 +no_defs +type=crs

    WKT2_2018 string:
    GEOGCRS["ETRS89",
        DATUM["European Terrestrial Reference System 1989",
            ELLIPSOID["GRS 1980",6378137,298.257222101,
                LENGTHUNIT["metre",1]]],
        PRIMEM["Greenwich",0,
            ANGLEUNIT["degree",0.0174532925199433]],
        CS[ellipsoidal,2],
            AXIS["geodetic latitude (Lat)",north,
                ORDER[1],
                ANGLEUNIT["degree",0.0174532925199433]],
            AXIS["geodetic longitude (Lon)",east,
                ORDER[2],
                ANGLEUNIT["degree",0.0174532925199433]],
        USAGE[
            SCOPE["unknown"],
            AREA["Europe - ETRS89"],
            BBOX[32.88,-16.1,84.17,40.18]],
        ID["EPSG",4258]]

