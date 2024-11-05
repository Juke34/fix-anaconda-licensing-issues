![](pages/images/Conda_logo.jpg){: style="height:100px"}

# Éviter les Pièges des Licences Anaconda : Guide Pratique

Les changements de licence d'Anaconda courant 2024 ont suscité quelques inquiétudes, en particulier dans des secteurs spécifiques tels que l'université, la recherche et les organisations à but non lucratif, qui se sont appuyés sur la plateforme en pensant qu'elle était disponible gratuitement.

Pour compliquer les choses, il y a souvent un malentendu sur ce qui est gratuit et ce qui ne l'est pas lorsqu'on utilise conda, le gestionnaire de paquets, par rapport aux canaux et aux distributions fournis par Anaconda.

## Qu'est-ce qui a changé ?

Le cœur des changements se trouve dans la définition d'Anaconda de « Organizational Use ». Selon les nouvelles [conditions de licence](https://legal.anaconda.com/policies/en/?name=terms-of-service#anaconda-terms-of-service), toute organisation (les entités gouvernementales et les organisations à but non lucratif) comptant au moins 200 employés ou contractants est désormais tenue d'acheter une licence payante pour utiliser le logiciel d'Anaconda ou des paquets provenant de canaux gérés par Anaconda.

## En bref

* **Conda**, le gestionnaire de paquets, est gratuit, open-source et accessible à tous.

* **Les paquets Conda provenant de canaux publics**  tels que **conda-forge**, **bioconda** ou tout autre canal communautaire, sont gratuits, open-source et accessible à tous.

* **Les paquets Conda gérés par Anaconda Inc.**  et **la distribution Anaconda** sont gratuite si et seulement si :
    - votre organisation compte moins de 200 employés, ou
    - Votre organisation est exemptée (par exemple, les étudiants ou les établissements d'enseignement, à condition qu’il soit utilisé pour des cours basés sur le programme).

## Mon organisation fait plus de 200 employés, comment eviter les éléments sous license?

* Bannir **Anaconda Distribution**.  
    Il faut se tourner vers d'autres alternative: Miniconda ou préférentiellement Miniforge.

* Bannir les canaux sous license.  
    Verifier et enlever les canaux sous license dans la configuration conda.  
    Eviter au tiers l'utilisation des canaux sous license (lors de partage d'environment).

Ce guide est fait pour vous aider dans ces démarches, voir plus. Bonne visite.