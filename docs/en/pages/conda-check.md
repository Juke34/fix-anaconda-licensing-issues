# Check and fix your installation for licensing problems

Here we show how to check your conda distribution to avoid any licensing issue.

## Anaconda

**Anaconda** is a distribution of not only Conda, but also over 150 scientific Python packages.  

!!! Warning
    * Anaconda is not free for company (even public) over 200 employees.  
    * Anaconda uses `defaults` channel that is not free for company (even public) over 200 employees.


    **You must remove it and install [Miniforge](../conda-installation.md) instead.**

## Miniconda

**Miniconda** is the lightweight version of Anaconda, the Conda package and environment manager.  

* Miniconda is free.

!!! Warning

    * Miniconda uses `defaults` channel that is not free for company (even public) over 200 employees.

    You can check the channels set for your installation as follow (it interrogates the .condarc file):

    ```bash
    conda config --show channels
    ```

    If any of these channels is listed ([see here for more information](../list_channels)): 

    * defaults
    * main 
    * anaconda
    * free
    * r 
    * mro
    * pro
    * archive
    * mro-archive
    * msys2 (part of defaults)

    **You must remove them.**  
    Here an example how to remove the `defaults` channel:

    ```bash
    conda config --remove channels defaults
    ```
        
    Check everything went well:

    ```bash
    conda config --show channels
    ```

## Miniforge

 **Miniforge**  is a minimal version of Conda, like Miniconda, but it uses `conda-forge` as its default package source. In other terms, everything is fine! 

You may check the channels set for you installation (it interrogates the .condarc file):

```bash
conda config --show channels
```

!!! Note
    * If you plan to add extra channels, be careful to avoid any of channel under Anaconda Inc. license:   defaults, main, anaconda, free, r, mro, pro, archive, mro-archive, msys2.

    * If you switch from Anaconda or Miniconda to Miniforge you may have the channels set up by your previous installation in the .condarc file. Please follow the procedure to remove the channels under Anaconda Inc license e.g `conda config --remove channels defaults`.

