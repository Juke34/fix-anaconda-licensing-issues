

|  | Anaconda | Miniconda (conda3-py312_24.9.2-0) | Miniforge (24.9.0-0) / Micromamba / Mambaforge| Micromamba |
| -- | -- | -- | -- | -- | 
| Préconisation | **Banir** son utilisation car il est sous license anaconda et utilise egalement des canaux sous lience anaconda. | **Attention**, bien qu'il soit libre d'utilisation, il faut bien configurer son installation pour éviter le canal `defaults`  sous license anaconda qui est utilisé par default. | **A privilégier**. Libre d'utilisation, et aucun canal sous license utilisé par defaut. Attention tout de même à ne pas rajouter manuellement des canaux sous license [voir ici](../conda-channels). | **A privilégier**. Libre d'utilisation, et aucun canal sous license utilisé par defaut. Attention tout de même à ne pas rajouter manuellement des canaux sous license [voir ici](../conda-channels). | 
| Créé et publié par Anaconda | Oui | Oui | Non |  Non |
| Contient conda | Oui | Oui | Oui | Oui | Oui (mamba) |
| Interface graphique | Oui | Non | Non | Non |
| Nb paquets préinstallés | 250+ | 72 | 74 | 0 |
| Espace d'installation nécessaire | ~2 Gb | ~550 Mb | ~314 Mb | ~15 Mb | 
| Description | Une distribution complète pour la data science, incluant Conda, Python, et environ 300 bibliothèques populaires comme NumPy, pandas, et Jupyter, prête à l’emploi. | Version minimale de la distribution Anaconda, qui installe seulement Conda, Python et leurs dépendances de base, sans les paquets Anaconda. | Une distribution minimale similaire à Miniconda, mais configurée pour utiliser conda-forge comme canal par défaut. | Micromamba est une version réduite du gestionnaire de paquets mamba (Ré-implementation de conda en C++). Il s'agit d'un exécutable lié statiquement avec une interface de ligne de commande séparée. Il n'a pas besoin d'un environnement de base et n'est pas livré avec une version par défaut de Python. |
| Inconvénients |  Taille élevée, licence payante pour les entreprises de plus de 200 employés. | Par défaut les paquets peuvent être téléchargés depuis les canaux sous licence Anaconda (defaults channel) | / | / |


