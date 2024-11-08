![](pages/images/Conda_logo.jpg){: style="height:100px"}

# Éviter les Pièges de la Licence Anaconda : Guide Pratique

Les modifications apportées à la licence 2024 par Anaconda ont suscité des inquiétudes, en particulier dans des secteurs tels que l'université, la recherche et les organisations à but non lucratif, qui considéraient jusqu'à présent que la plateforme était librement accessible.

Deux difficulés importantes aujourd'hui sont la distinction :  

  - entre l'utilisation gratuite de Conda, le gestionnaire de paquets lui-même, et la distribution sous licence appelé anaconda, qui est une interface graphique intégrant Conda. 
  - entre les canaux libres et les canaux sous licence gérés par Anaconda (les canaux définissent le lieu où Conda cherche les paquets).

## Qu'est-ce qui a changé ?

Le cœur des changements se trouve dans la définition d'Anaconda de « Organizational Use ». Selon les nouvelles [conditions de licence](https://legal.anaconda.com/policies/en/?name=terms-of-service#anaconda-terms-of-service), toute organisation (les entités gouvernementales et les organisations à but non lucratif) comptant au moins 200 employés ou contractants est désormais tenue d'acheter une licence payante pour utiliser le logiciel d'Anaconda ou des paquets provenant de canaux gérés par Anaconda.

## En bref

* **Conda**, le gestionnaire de paquets, est gratuit, open-source et accessible à tous.

* **Les paquets Conda provenant de canaux publics**  tels que **conda-forge**, **bioconda** ou tout autre canal communautaire, sont gratuits, open-source et accessible à tous.

* **Les paquets Conda gérés par Anaconda Inc.**  et **la distribution Anaconda** sont gratuite si et seulement si :
    - votre organisation compte moins de 200 employés, ou
    - Votre organisation est exemptée (par exemple, les étudiants ou les établissements d'enseignement, à condition qu’il soit utilisé pour des cours basés sur le programme).

## Comment eviter les éléments sous license?

* **Bannir Anaconda Distribution**  
    Il faut se tourner vers d'autres alternative: Miniconda ou préférentiellement Miniforge. <[voir ici](./pages/conda-distrib)>  
    Installer Miniforge <[voir ici](./pages/conda-installation)>

* **Bannir [les canaux sous license](./pages/conda-channels/)**  
    Verifier et enlever les canaux sous license dans la configuration conda. <[voir ici](./pages/conda-check)>  
    Eviter au tiers l'utilisation des canaux sous license (lors de partage d'environment). <[voir ici](./pages/conda-share)>

Ce guide est fait pour vous aider dans ces démarches, voir plus. Bonne visite.