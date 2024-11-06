When following tool installation instruction it is common to see this way of doing:

```
conda install -c defaults -c conda-forge package_name
```

or

```
conda install --channel defaults --channel conda-forge package_name
```

**-c** and **--channel** allows to specify one or more channels where conda will fetch the package to be installed.  
In this example, conda will search first defaults and then conda-forge if the package is not found in the first.  
When you explicitly specify channels with **-c** and **--channel** in the conda install command, Conda will use only the channels specified in the command and ignore those defined in your local configuration (the .condarc file).

!!! Warning
    Check carefully your command to avoid that **-c** and **--channel** point to channels under Anaconda Inc. license.