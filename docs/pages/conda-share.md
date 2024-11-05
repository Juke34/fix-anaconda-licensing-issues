Saving an environment is a good practice. The generated backup file is really light and will allow you to share the environmnet with collaborators or easily re-use the same environment on another computer.

Depending the way you saved your environment i.e:

`conda env export > environment.yml`  
`conda env export --from-history > environment.yml`  
`conda env export  --no-builds > environment.yml`  

you will have a `channels` section on top:  

```bash
channels:
- conda-forge
- bioconda
``` 

The information hold by the `channels` section have priority over the channels configured in your local conda configuration file (`.condarc`). When building an environement from this file, if a package is not found among the listed channels, then the channels defined in your local conda configuration (`.condarc`) will be used.  

When sharing the file with someone else, if this person did not deactivate the `defaults` channel in its local conda configuration, she/he may use anaconda licensed `defaults` channel.

To avoid this issue you should add the  `- nodefaults` channel in the `channels`section of your saved yaml environment, which will deactivate the `defaults` channel from the local conda configuration (`.condarc`) of the computer using it.

!!! Warning "**Before sharing an environemnt with someone, verify the `channels` section of the yaml file**"
    * Verify to not have any of licensed channels : defaults, main, anaconda, free, r, mro, pro, archive, mro-archive, msys2
    * add `- nodefaults` to deactivate the `defaults` channel from `.condarc`
