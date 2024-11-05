# Installing Conda

Here we show how to install conda without any licensing issue.

## Download

!!! info "Different Condas"

    There are several Conda-related tool you may have encountered ([see here for more information](../conda-distrib/)):  

    * **Miniforge**  is a minimal version of Conda, like Miniconda, but it uses Conda-forge as its default package source, which is free to use.  
    * **Miniconda** which is the lightweight version of Anaconda, the Conda package and environment manager. /!\ contains defaults channels that are not totaly free!  
    * **Anaconda**, which is a distribution of not only Conda, but also over 150 scientific Python packages. It's generally better to stick with only Conda, *i.e.* installing with Miniforege, Mambaforge or Miniconda, rather than installing 3 GB worth of packages you may not even use. /!\ The license is not free for company (even public) over 200 employees. /!\/!\ contains defaults channels that are not totaly free!
    

**Install Miniforge**  

Conda is installed by downloading and executing an installer, but which version you need depends on your operating system.  

Choose the appropriate installer from the list you can found here:  
[https://conda-forge.org/download/](https://conda-forge.org/download/) or here [https://github.com/conda-forge/miniforge](https://github.com/conda-forge/miniforge).  
Then copy the link and download the installer on your computer, see example below: 

```bash
# Download Miniconda3 installer for 64-bit Linux
curl -L https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh -O
```
or
```bash
# Download Miniconda3 installer for 64-bit Linux
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh 
```

## Install

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
Then press ![](../images/space-key.png){: style="height:30px;"} several times until reaching the next question

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


## Configure

### Auto activation

By default conda will be activated to every new terminal you will open (in the `base` environment).  To deactivate this behaviour run:

```bash
conda config --set auto_activate_base false
```

### Channels

You’re all set! Miniforge only includes the conda-forge channel, which is free to use.  
To verify, you can type the following command (it interrogates the .condarc file):

```bash
conda config --show channels
```

You can add any free channel e.g. bioconda as follow:

```bash
conda config --add channels bioconda
conda config --add channels conda-forge
conda config --set channel_priority strict
```


!!! Note
    If your Miniforge installation comes after Anaconda or Miniconda uninstallation, you may have the channels set from your previous installation in the .condarc file. It may explain why you do not have only the `conda-forge` channel as expected. Please follow the procedure to remove all the channels under Anaconda Inc license i.e `conda config --remove channels defaults`.