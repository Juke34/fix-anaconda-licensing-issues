Even if you correctly configure the channels into which you download packages to avoid licensed channels ([list of licensed channels](../conda-channels), [check and fix your installation for licensing problems](../conda-check)), at the institutional level it may be difficult to ensure everyone is avoiding the Anaconda Inc. license trap.

A radical solution is to ask network administrators to block downloads from Anaconda Inc. licensed channels:

```
https://conda.anaconda.org/pkgs/main
https://conda.anaconda.org/pkgs/free
https://conda.anaconda.org/pkgs/r
https://conda.anaconda.org/pkgs/mro
https://conda.anaconda.org/pkgs/pro
https://conda.anaconda.org/pkgs/archive
https://conda.anaconda.org/pkgs/mro-archive
https://conda.anaconda.org/pkgs/msys2
```

!!! Warning 
    You might be tempted to block the address `https://conda.anaconda.org` directly, but this is a bad idea.
    Indeed, packages form community channels free and open-source like **conda-forge** and **bioconda** are also hosted there (https://conda.anaconda.org/conda-forge, https://conda.anaconda.org/bioconda). At the time beeing, no other ressource host to download these packages is available.