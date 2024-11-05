# Installation de Conda

Nous montrons ici comment installer Conda sans problème de licence.

## Télécharger

!!! info "Différents Condas"
    Il y a plusieurs outils liés à Conda que vous avez pu rencontrer ([voir ici pour plus d'informations](../conda-distrib/)) :

    * **Miniforge** est une version minimale de Conda, comme Miniconda, mais il utilise Conda-forge comme source de paquets par défaut, qui est libre d'utilisation.  
    * **Miniconda** qui est la version légère d'Anaconda, le gestionnaire de paquets et d'environnement de Conda.  
    /!\ il utilise des canaux par défaut qui ne sont pas totalement libres !  
    * **Anaconda**, qui est une distribution non seulement de Conda, mais aussi de plus de 150 paquets scientifiques Python. Il est généralement préférable de s'en tenir à Conda, c'est-à-dire d'installer Miniforge, Mambaforge ou Miniconda, plutôt que d'installer 3 Go de paquets que vous n'utiliserez peut-être même pas.  
    /!\ La licence n'est pas gratuite pour les entreprises (même publiques) de plus de 200 employés.  
    /!\ /!\ il utilise des canaux par défaut qui ne sont pas totalement libres ! 

**Installer Miniforge**

Conda est installé en téléchargeant et en exécutant un programme d'installation, mais la version dont vous avez besoin dépend de votre système d'exploitation.  

Choisissez le programme d'installation approprié dans la liste que vous trouverez ici :  
[https://conda-forge.org/download/](https://conda-forge.org/download/) ou ici [https://github.com/conda-forge/miniforge](https://github.com/conda-forge/miniforge).  

Copiez ensuite le lien et téléchargez le programme d'installation sur votre ordinateur (voir l'exemple ci-dessous) : 
```bash
# Télécharger le programme d'installation de Miniforge pour Linux 64 bits
curl -L https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh -O
```
ou
```bash
# Télécharger le programme d'installation de Miniforge pour Linux 64 bits
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh 
```

## Installation

Vous pouvez maintenant exécuter le programme d'installation :

```bash
bash Miniforge3-Linux-x86_64.sh
```

Le programme d'installation vous posera des questions pendant l'installation :

<div class="custom-terminal">
In order to continue the installation process, please review the license agreement.<br>
Please, press ENTER to continue <br> 
>>> 
</div>

Appuyez sur ![](../images/enter-key.png){: style="height:30px;"}  
Appuyez ensuite sur  ![](../images/space-key.png){: style="height:30px;"} plusieurs fois jusqu'à la question suivante.

- Do you accept the license terms?  
 Yes  
- Do you accept the installation path or do you want to choose a different one?  
Appuyez sur  ![](../images/enter-key.png){: style="height:30px;"}   
- Do you wish to update your shell profile to automatically initialize conda?  
Yes

Redémarrez votre shell pour que les réglages dans `~/.bashrc` or `~/.bash_profile` prennent effet. Ou lancez:

```
source ~/.bashrc 
```

Vous pouvez vérifier que l'installation a fonctionné en lançant le programme :

```bash
conda --version
```

Vous pouvez maintenant vous débarrasser de l'installateur, vous n'en avez plus besoin :

```bash
rm Miniforge3-Linux-x86_64.sh
```


## Configuration

### Activation automatique

Par défaut, conda sera activé pour chaque nouveau terminal que vous ouvrirez (dans l'environnement `base`).  Pour désactiver ce comportement, exécutez :

```bash
conda config --set auto_activate_base false
```

### Canaux

Vous êtes prêts ! Miniforge n'inclut que le canal `conda-forge`, dont l'utilisation est gratuite.  
Pour vérifier, vous pouvez taper la commande suivante (elle interroge le fichier .condarc) :


```bash
conda config --show channels
```

Vous pouvez ajouter n'importe quel canal gratuit, par exemple `bioconda`, comme suit :

```bash
conda config --add channels bioconda
conda config --add channels conda-forge
conda config --set channel_priority strict
```


!!! Note
    Si votre installation de Miniforge vient après la désinstallation d'Anaconda ou de Miniconda, il se peut que vous ayez les canaux de votre installation précédente dans le fichier .condarc. Cela peut expliquer pourquoi vous n'auriez pas seulement le canal `conda-forge` comme prévu. Veuillez suivre la procédure pour supprimer tous les canaux sous licence Anaconda Inc,  par exemple `conda config --remove channels defaults`.