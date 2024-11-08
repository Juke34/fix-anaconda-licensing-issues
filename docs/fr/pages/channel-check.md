##### Vérifier les canaux

Pour vérifier les canaux utilisés par votre installation, vous pouvez taper la commande suivante :

```bash
conda config --show channels
```

Vous devriez voir quelque chose comme :

<div class=custom-terminal>
channels:<br>
&nbsp;&nbsp;- conda-forge
</div>>

!!! warning "Attention"
    Si vous voyez d'autres canaux, cela peut être dû à une installation précédente de Conda.  
    [Vérifiez qu'aucun canal sous licence Anaconda Inc. ne figure parmi eux.](../conda-check/#verifier-les-canaux)


##### Ajouter des canaux gratuits supplémentaires

Vous pouvez ajouter n'importe quel canal gratuit, par exemple `bioconda`, comme suit :

```bash
conda config --add channels bioconda
```

{%
include "fr/pages/channel-check-note.md"
%}

##### Partager des environnements en toute sécurité

Pour savoir pourquoi ajouter cette ligne supplémentaire [voir ici](../conda-share)  

```bash
conda config --add channels nodefaults
```

##### Reproductibilité 

Il est recommandé de définir une `priorité stricte des canaux`.  
Cela peut accélérer considérablement les opérations de Conda et réduire les problèmes d'incompatibilité des paquets.

```bash
conda config --set channel_priority strict
```