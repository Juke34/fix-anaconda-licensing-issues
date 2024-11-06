Lorsque l'on suit les instructions d'installation d'un outil, il est courant de voir cette façon de faire :

```
conda install -c defaults -c conda-forge nom_du_paquet
```

ou

```
conda install --channel defaults --channel conda-forge nom_du_paquet
```

**-c** et **--channel** permettent de spécifier un ou plusieurs canaux dans lesquels conda va chercher le paquet à installer.  
Dans cet exemple, conda cherchera d'abord defaults puis conda-forge si le paquet n'est pas trouvé dans le premier.  
Lorsque vous spécifiez explicitement des canaux avec **-c** et **--channel** dans la commande conda install, Conda n'utilisera que les canaux spécifiés dans la commande et ignorera ceux définis dans votre configuration locale (le fichier .condarc).

!!! Warning "Attention"
    Vérifiez soigneusement votre commande pour éviter que **-c** et **--channel** ne pointent vers des canaux sous licence Anaconda Inc.