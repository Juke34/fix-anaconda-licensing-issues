# Installer conda sans problème de license

Nous présentons ici deux solutions pour installer Conda sans problèmes de licence Anaconda :

 * Miniforge une version allégée de Conda qui utilise `conda-forge` comme source de paquets par défaut (canal), qui est libre d'utilisation.
 * Micromamba une version minimale de Conda (il s'agit en fait de `mamba`, une implémentation de Conda en C++) qui évite par défaut tout canal sous licence Anaconda.

Pour une vue d'ensemble des différentes distributions de Conda [voir ici](../conda-distrib).

## Miniforge

### Télécharger

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

### Installer

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

### Configurer les canaux

Même si `Miniforge` n'inclut que le canal `conda-forge`, qui est libre d'utilisation, il est toujours bon de vérifier l'installation.

{%
include "fr/pages/channel-check.md"
%}


### Activation automatique

Par défaut, conda sera activé pour chaque nouveau terminal que vous ouvrirez (dans l'environnement `base`).  Pour désactiver ce comportement, exécutez :

```bash
conda config --set auto_activate_base false
```

## Micromamba

Micromamba est un exécutable entièrement lié de manière statique et autonome. Cela signifie que l'environnement de base est complètement vide. La configuration de micromamba est légèrement différente, à savoir que tous les environnements et les caches seront créés par défaut sous la variable d'environnement MAMBA_ROOT_PREFIX. Il n'y a pas non plus de .condarc/.mambarc pré-configuré livré avec micromamba (ils sont cependant toujours lus s'ils sont présents).

!!! Note
    Lorsque l'on utilise micromamba, les commandes `conda` sont remplacées par `micromamba` !

### Télécharger et installer

Micromamba est installé en téléchargeant et en exécutant un programme d'installation :  

```bash
# Télécharger le programme d'installation de Micromamba 
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
```

Le programme d'installation vous posera des questions pendant l'installation :

<div class="custom-terminal">
Micromamba binary folder? [~/.local/bin]
</div>

Appuyer sur la touche ![](../images/enter-key.png){: style="height:30px;"}  

<div class="custom-terminal">
Init shell (bash)? [Y/n]
</div>

Appuyer sur la touche ![](../images/enter-key.png){: style="height:30px;"}   

<div class="custom-terminal">
Configure conda-forge? [Y/n]
</div>

Appuyer sur la touche ![](../images/enter-key.png){: style="height:30px;"}   

<div class="custom-terminal">
Prefix location? [~/micromamba]
</div>

Appuyer sur la touche ![](../images/enter-key.png){: style="height:30px;"}   

Pour prendre en compte les modifications, redémarrez votre shell ou exécutez :

```
# (or ~/.bash_profile, ~/.zshrc, ~/.xonshrc, ~/.config/fish/config.fish, ...)
source ~/.bashrc 
```

Vous pouvez vérifier que l'installation a fonctionné en lançant le programme :

```bash
micromamba --version
```

### Configurer les canaux

Même si `Micromamba` n'inclut que le canal `conda-forge`, qui est libre d'utilisation, il est toujours bon de vérifier l'installation.

{%
include "fr/pages/channel-check.md"
%}
