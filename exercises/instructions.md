# Install PROJ

We will be using the `conda` command line system to install and run PROJ
in. In short, `conda` let's you install and update various command line
tools in an easy way.You need to download the correct installers for your system. Find the Miniconda installer
[here](https://repo.continuum.io/miniconda/).

This guide will demonstrate how to make the installation on Windows but
the steps are similar on other systems as well.

Installation steps:

1. Run the installer
2. When asked, select "Just Me" (the default option)
3. The default installation folder is fine, continue
4. Finish the installation

After the installation is done open the "Anaconda Prompt" from the Windows start
menu. When the prompt is open, enter the command

    conda install proj -c conda-forge

Wait a bit until the installation is finished. Once the installation is over you
can try issueing a PROJ command:

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


# How to fill out the PROJ tutorial exercises

All the exercises are made as `gie` tests where one or more inputs are missing.
gie files are plain text files which you can edit in your favorite text editor.
If you don't have a favorite text editor you can use notepad, it is fine for this!

Replace occurrences of `<your answer here>` with the relevant input. Below
is an annotated example of a complete gie test. Your objective is to fill out
the exercises from 1 and onwards in a similar fashion.

Below is a simple exercise before the answer has been filled in
Below is

```
1. Set up an operation that returns the input it is given
-------------------------------------------------------------------------------
operation   <your answer here>
tolerance   10 mm

accept      12.3    45.6
expect      12.3    45.6
-------------------------------------------------------------------------------
```

An annotated answer could look like this:

```
<gie>
operation   +proj=latlon    # The latlon "projection" returns the same output as
                            # given in the input
tolerance   10 mm

accept      12.3    45.6
expect      12.3    45.6
</gie>
```

The `gie` application can be used to check if the exercise has been answered
correctly:

```
gie exercises\<exercise_name>.gie
```

If all answers are correct `gie` will return output similar to:

```
-------------------------------------------------------------------------------
Reading file 'exercises\instructions.md'
-------------------------------------------------------------------------------
total:  1 tests succeeded,  0 tests skipped,  0 tests failed.
-------------------------------------------------------------------------------
```

If incorrect, `gie` will output something like:

```
-------------------------------------------------------------------------------
Reading file 'exercises\instructions.md'
     -----
     FAILURE in instructions.md(48):
     expected: 12.3 45.6
     got:      1369229.736757265171   5685937.873489554040
     deviation:  999999999.999000 mm,  expected:  10.000000 mm
-------------------------------------------------------------------------------
total:  0 tests succeeded,  0 tests skipped,  1 tests FAILED!
-------------------------------------------------------------------------------
```

Where the number of failing exercises (or tests in `gie` terminology) is given, as
well as the line number of the failing test (in parenthesis after the file name).
