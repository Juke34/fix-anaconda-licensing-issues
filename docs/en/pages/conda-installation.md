# Install conda without license problems

Here, we present three solutions for using the Conda package ecosystem without Anaconda license problems:

* Miniforge, a light version of Conda that uses `conda-forge` as its default package source (channel), which is free to use.
* Micromamba, a minimal version of Conda (actually, `mamba`, a Conda implementation in C++) that avoids any channel under the Anaconda license by default.
* Pixi, a lightweight package manager implementation that uses the Conda package ecosystem. It is free to use and open source.

For an overview of the different conda distribution [see here](../conda-distrib).

## Miniforge

### Download

Conda is installed by downloading and executing an installer, but which version you need depends on your operating system.  

Choose the appropriate installer from the list you can found here:  
[https://conda-forge.org/download/](https://conda-forge.org/download/) or here [https://github.com/conda-forge/miniforge](https://github.com/conda-forge/miniforge).  
Then copy the link and download the installer on your computer, see example below: 

```bash
# Download Miniforge installer for 64-bit Linux
curl -L https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh -O
```
or
```bash
# Download Miniforge installer for 64-bit Linux
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh 
```

### Install

Now you can execute the installer:

```bash
bash Miniforge3-Linux-x86_64.sh
```

The installer will ask you questions during the installation:

<div class="custom-terminal">
In order to continue the installation process, please review the license agreement.<br>
Please, press ENTER to continue <br> 
>>> 
</div>

Press ![](../images/enter-key.png){: style="height:30px;"}  
Then press ![](../images/space-key.png){: style="height:30px;"} several times until reaching the next question.

- Do you accept the license terms?  
 Yes  
- Do you accept the installation path or do you want to choose a different one?  
Press ![](../images/enter-key.png){: style="height:30px;"}   
- Do you wish to update your shell profile to automatically initialize conda?  
Yes

Restart your shell so that the settings in `~/.bashrc` or `~/.bash_profile` can take
effect. Or run  
```
source ~/.bashrc 
```

You can verify that the installation worked by running:

```bash
conda --version
```

You can now get rid of the installer, you don't need it anymore

```bash
rm Miniforge3-Linux-x86_64.sh
```

### Configure Channels

Even if `Miniforge` only includes the `conda-forge` channel, which is free to use, it is always good to check the installation.

{%
include "en/pages/channel-check.md"
%}

### Auto activation

By default conda will be activated to every new terminal you will open (in the `base` environment).  To deactivate this behaviour run:

```bash
conda config --set auto_activate_base false
```


## Micromamba

Micromamba is a fully statically-linked, self-contained, executable. This means that the base environment is completely empty. The configuration for micromamba is slightly different, namely all environments and cache will be created by default under the MAMBA_ROOT_PREFIX environment variable. There is also no pre-configured .condarc/.mambarc shipped with micromamba (they are however still read if present).

!!! Note
    When using micromamba, the `conda` commands are replaced by `micromamba`!

### Download and Install

Micromamba is installed by downloading and executing an installer:  

```bash
# Download Micromamba installer 
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
```

The installer will ask you questions during the installation:

<div class="custom-terminal">
Micromamba binary folder? [~/.local/bin]
</div>

Press ![](../images/enter-key.png){: style="height:30px;"}  

<div class="custom-terminal">
Init shell (bash)? [Y/n]
</div>

Press ![](../images/enter-key.png){: style="height:30px;"}   

<div class="custom-terminal">
Configure conda-forge? [Y/n]
</div>

Press ![](../images/enter-key.png){: style="height:30px;"}   

<div class="custom-terminal">
Prefix location? [~/micromamba]
</div>

Press ![](../images/enter-key.png){: style="height:30px;"}   

To take the changes into account restart your shell or run:
```
# (or ~/.bash_profile, ~/.zshrc, ~/.xonshrc, ~/.config/fish/config.fish, ...)
source ~/.bashrc 
```

You can verify that the installation worked by running:

```bash
micromamba --version
```

### Configure Channels

Even if `Micromamba` only includes the `conda-forge` channel, which is free to use, it is always good to check the installation.

{%
include "en/pages/channel-check.md"
%}

## Pixi

Pixi provides thorough [installation and setup instructions in its documentation](https://pixi.sh/latest/#installation).
Review that documentation for the latest installation methods.
For convenience, the typical methods follow.

For Linux and macOS, an installer is available:

```shell
curl -fsSL https://pixi.sh/install.sh | bash
```

or install with [the `pixi` Homebrew formula](https://formulae.brew.sh/formula/pixi):

```shell
brew install pixi
```

For Windows:

```powershell
powershell -ExecutionPolicy ByPass -c "irm -useb https://pixi.sh/install.ps1 | iex"
```

To add channels to your project configuration in `pixi.toml`, use

```shell
pixi project channel add conda-forge
```
