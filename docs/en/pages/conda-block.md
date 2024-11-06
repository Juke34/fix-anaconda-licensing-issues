Even if you correctly configure the channels into which you download packages to avoid licensed channels ([list of licensed channels](../conda-channels), [check and fix your installation for licensing problems](../conda-check)), at the institutional level it may be difficult to ensure everyone is avoiding the Anaconda Inc. license trap.

A radical solution is to ask network administrators to block downloads from Anaconda Inc. licensed channels:

```
https://repo.anaconda.com/pkgs/main/
https://conda.anaconda.org/main/ 
https://conda.anaconda.org/anaconda/ 
https://repo.anaconda.com/pkgs/r/
https://conda.anaconda.org/r/
https://repo.anaconda.com/pkgs/msys2/
https://conda.anaconda.org/msys2/
https://repo.anaconda.com/pkgs/free/
https://conda.anaconda.org/free/
https://repo.anaconda.com/pkgs/archive/
https://repo.anaconda.com/pkgs/pro/
https://conda.anaconda.org/anaconda-extras/
https://repo.anaconda.com/pkgs/mro
https://repo.anaconda.com/mro-archive
```

More information [here](https://docs.anaconda.com/working-with-conda/reference/default-repositories/).

!!! Warning 
    You might be tempted to block the address `https://conda.anaconda.org` directly, but this is a bad idea.
    Indeed, packages form community channels free and open-source like **conda-forge** and **bioconda** are also hosted there (https://conda.anaconda.org/conda-forge, https://conda.anaconda.org/bioconda). At the time beeing, no other ressource host to download these packages is available.