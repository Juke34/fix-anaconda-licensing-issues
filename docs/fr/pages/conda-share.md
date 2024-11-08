Sauvegarder un environnement est une bonne pratique. Le fichier de sauvegarde généré est très léger et vous permettra de partager l'environnement avec des collaborateurs ou de réutiliser facilement le même environnement sur un autre ordinateur.

En fonction de la manière dont vous avez sauvegardé votre environnement, c'est-à-dire

`conda env export > environment.yml`  
`conda env export --from-history > environment.yml`  
`conda env export  --no-builds > environment.yml`  

vous aurez une section `channels` en haut : 

```bash
channels:
- conda-forge
- bioconda
``` 

Les informations contenues dans la section `channels` sont prioritaires sur les canaux configurés dans votre fichier de configuration local de conda (`.condarc`). Lors de la construction d'un environnement à partir de ce fichier, si un paquet n'est pas trouvé parmi les canaux listés, alors les canaux définis dans votre configuration locale de conda (`.condarc`) seront utilisés.

Lorsque vous partagez le fichier avec quelqu'un d'autre, si cette personne n'a pas désactivé le canal `defaults` dans sa configuration conda locale, elle peut utiliser le canal `defaults` sous licence anaconda.

Pour éviter ce problème, vous devriez ajouter le canal `- nodefaults` dans la section `channels` de votre environnement yaml sauvegardé, ce qui désactivera le canal `defaults` de la configuration locale de conda (`.condarc`) de l'ordinateur qui l'utilise.

Pour plus de détails, voir la [documentation pertinente de conda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually).

!!! Warning "**Avant de partager un environnement avec quelqu'un, vérifiez la section `channels` du fichier yaml**"
    * Vérifier qu'il n'y a pas de canaux sous licence : defaults, main, anaconda, free, r, mro, pro, archive, mro-archive, msys2
    * ajouter `- nodefaults` pour désactiver le canal `defaults` de `.condarc`