# Vérifier et corriger les problèmes de license de son installation

Nous montrons ici comment vérifier votre distribution conda afin d'éviter tout problème de licence.

## Anaconda

**Anaconda** est une distribution non seulement de Conda, mais aussi de plus de 150 paquets scientifiques Python.  

!!! Warning "Attention"
    * Anaconda n'est pas gratuit pour les entreprises (même publiques) de plus de 200 employés.  
    * Anaconda utilise le canal `defaults` qui n'est pas libre pour les entreprises (même publiques) de plus de 200 employés.


    **Vous devez le supprimer et installer [Miniforge](../conda-installation.md) à la place.**

## Miniconda

**Miniconda** is the lightweight version of Anaconda, the Conda package and environment manager.  

* Miniconda est gratuit.

!!! Warning "Attention"

    * Miniconda utilise le canal `defaults` qui n'est pas libre pour les entreprises (même publiques) de plus de 200 employés.

    Vous pouvez vérifier les canaux définis pour votre installation comme suit (il interroge le fichier .condarc) :

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

## Miniforge

 **Miniforge**  est une version minimale de Conda, comme Miniconda, mais elle utilise `conda-forge` comme source de paquet par défaut. En d'autres termes, tout va bien !

Vous pouvez vérifier les canaux définis pour votre installation (il interroge le fichier .condarc) :

```bash
conda config --show channels
```

!!! Note
    * Si vous prévoyez d'ajouter des canaux supplémentaires, veillez à éviter toute chaîne sous licence Anaconda Inc. : defaults, main, anaconda, free, r, mro, pro, archive, mro-archive, msys2.

    * Si vous passez d'Anaconda ou Miniconda à Miniforge, il se peut que les canaux définis par votre installation précédente soient présents dans le fichier .condarc. Veuillez suivre la procédure pour supprimer les canaux sous la licence Anaconda Inc, par exemple `conda config --remove channels defaults`.

