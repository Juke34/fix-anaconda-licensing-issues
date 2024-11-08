##### Check channels

To verify the channels used by your installation you can type the following command:

```bash
conda config --show channels
```

You should see something like:

<div class=custom-terminal>
channels:<br>
&nbsp;&nbsp;- conda-forge
</div>>

!!! warning
    If you see other channels, this may be due to a previous Conda installation.  
    [Check that no Anaconda Inc. licensed channel is among them.](../conda-check/#check-channels)


##### Add extra free channels

You can add any free channel e.g. `bioconda` as follow:

```bash
conda config --add channels bioconda
```

{%
include "en/pages/channel-check-note.md"
%}

##### Sharing environments safely

For explanation why adding this extra line [see here](../conda-share)  

```bash
conda config --add channels nodefaults
```

##### Reproducibility 

Is is recommended to set a `strict channel priority`.  
It can dramatically speed up conda operations and also reduce package incompatibility problems.

```bash
conda config --set channel_priority strict
```