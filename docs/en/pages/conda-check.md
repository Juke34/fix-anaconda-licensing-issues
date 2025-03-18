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
    Follow instruction to get rid of channels under anaconda inc. license: [here](#check-channels)


{%
include "en/pages/channel-check-note.md"
%}

## Miniforge

 **Miniforge**  is a minimal version of Conda, like Miniconda, but it uses `conda-forge` as its default package source. In other terms, everything is supposed to be fine!  

{%
include "en/pages/channel-check-warning.md"
%}

{%
include "en/pages/channel-check-note.md"
%}

## Micromamba

 **Micromamba**  is the lightest version of "Conda", it comes with zero preinstalled packages, no base environment and the required installation space is just the executable.  
`conda-forge` is the only default package source you can set up during the installation procedure. In other terms, everything is supposed to be fine!  

{%
include "en/pages/channel-check-warning.md"
%}

{%
include "en/pages/channel-check-note.md"
%}

## Pixi

**Pixi** is a lightweight, project-centric package management tool that uses the Conda ecosystem but presents a different command line tool.
It is a single executable written in Rust.
It safely uses only `conda-forge` by default.

Run `pixi project channel list` to see configured channels or look for the `channels` key in `pixi.toml`.

{%
include "en/pages/channel-check-warning.md"
%}

{%
include "en/pages/channel-check-note.md"
%}

## Check channels


Check the channels set for your installation as follow:

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
* msys2

**You must remove them.**  
Here an example how to remove the `defaults` channel:

```bash
conda config --remove channels defaults
```
        
Check everything went well:

```bash
conda config --show channels
```
