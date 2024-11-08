# Vérifier et corriger les problèmes de license de son installation

Nous montrons ici comment vérifier votre distribution conda afin d'éviter tout problème de licence.

## Anaconda

**Anaconda** est une distribution non seulement de Conda, mais aussi de plus de 150 paquets scientifiques Python.  

!!! Warning "Attention"
    * Anaconda n'est pas gratuit pour les entreprises (même publiques) de plus de 200 employés.  
    * Anaconda utilise le canal `defaults` qui n'est pas libre pour les entreprises (même publiques) de plus de 200 employés.


    **Vous devez le supprimer et installer [Miniforge](../conda-installation.md) à la place.**

## Miniconda

**Miniconda** est la version allégée d'Anaconda, le gestionnaire de paquets et d'environnement Conda.

* Miniconda est gratuit.

!!! Warning "Attention"

    * Miniconda utilise le canal `defaults` qui n'est pas libre pour les entreprises (même publiques) de plus de 200 employés.  
    Suivez les instructions pour vous débarrasser des chaînes sous licence anaconda inc. : [ici](#verifier-les-canaux)

{%
include "fr/pages/channel-check-note.md"
%}

## Miniforge

 **Miniforge**  est une version minimale de Conda, comme Miniconda, mais elle utilise `conda-forge` comme source de paquet par défaut. En d'autres termes, tout va bien !

{%
include "fr/pages/channel-check-warning.md"
%}

{%
include "fr/pages/channel-check-note.md"
%}

## Micromamba

**Micromamba** est la version la plus légère de "Conda", elle est livrée avec zéro package préinstallé, aucun environnement de base et l'espace d'installation requis est juste l'exécutable.  
`conda-forge` est la seule source de paquets par défaut que vous pouvez configurer pendant la procédure d'installation. En d'autres termes, tout est censé bien se passer !  

{%
include "fr/pages/channel-check-warning.md"
%}

{%
include "fr/pages/channel-check-note.md"
%}

## Vérifier les canaux

Vérifiez les canaux réglés pour votre installation comme suit :

```bash
conda config --show channels
```

Si l'un de ces canaux est répertorié ([voir ici pour plus d'informations](../list_channels)): 

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

**Vous devez les supprimer.**  
Voici un exemple de suppression du canal `defaults` :
    
```bash
conda config --remove channels defaults
```
        
Vérifiez que tout s'est bien passé :

```bash
conda config --show channels
```