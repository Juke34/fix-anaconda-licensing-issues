Même si vous configurez correctement les canaux dans lesquels vous téléchargez les paquets pour éviter les canaux sous licence ([liste des canaux sous licence](../conda-channels), [vérifiez et corrigez votre installation pour les problèmes de licence](../conda-check)), au niveau institutionnel, il peut être difficile de s'assurer que tout le monde évite le piège de la licence d'Anaconda Inc.

Une solution radicale consiste à demander aux administrateurs du réseau de bloquer les téléchargements à partir des canaux sous licence Anaconda Inc.:

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
Plus d'information [ici](https://docs.anaconda.com/working-with-conda/reference/default-repositories/) et [ici](https://repo.anaconda.com/pkgs/).

!!! Warning "Attention" 
    Vous pourriez être tenté de bloquer l'adresse `https://conda.anaconda.org` directement, mais c'est une mauvaise idée.  
    En effet, les paquets des canaux communautaires libres et open-source comme **conda-forge** et **bioconda** y sont également hébergés (https://conda.anaconda.org/conda-forge, https://conda.anaconda.org/bioconda). A l'heure actuelle, il n'existe pas d'autre hébergeur de ressources pour télécharger ces paquets.