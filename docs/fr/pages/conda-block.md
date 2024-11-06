Même si vous configurez correctement les canaux dans lesquels vous téléchargez les paquets pour éviter les canaux sous licence ([liste des canaux sous licence](../conda-channels), [vérifiez et corrigez votre installation pour les problèmes de licence](../conda-check)), au niveau institutionnel, il peut être difficile de s'assurer que tout le monde évite le piège de la licence d'Anaconda Inc.

Une solution radicale consiste à demander aux administrateurs du réseau de bloquer les téléchargements à partir des canaux sous licence Anaconda Inc.:

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

!!! Warning "Attention" 
    Vous pourriez être tenté de bloquer l'adresse `https://conda.anaconda.org` directement, mais c'est une mauvaise idée.  
    En effet, les paquets des canaux communautaires libres et open-source comme **conda-forge** et **bioconda** y sont également hébergés (https://conda.anaconda.org/conda-forge, https://conda.anaconda.org/bioconda). A l'heure actuelle, il n'existe pas d'autre hébergeur de ressources pour télécharger ces paquets.