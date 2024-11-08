![](pages/images/Conda_logo.jpg){: style="height:100px"}

# Avoiding the Pitfalls of the Anaconda License: A Practical Guide

The 2024 license changes by Anaconda have raised concerns, particularly among sectors like academia, research, and non-profits, which previously assumed that the platform was freely accessible.

Two significant challenges now are the distinction:  

  - between free usage of Conda, the package manager itself, and the licensed Anaconda distribution, which is a graphical interface integrating conda. 
  - between the free channels versus the licensed channels managed by Anaconda (channels define where conda will fetch the package).

## What has changed?

The primary change centers on Anaconda’s updated definition of “Organizational Use”. Under the new [license conditions](https://legal.anaconda.com/policies/en/?name=terms-of-service#anaconda-terms-of-service), any organization (including government agencies and non-profits) with 200 or more employees or contractors must now acquire a paid license to use Anaconda’s software or packages provided via Anaconda’s managed channels.

## In brief

* **Conda**, the package manager, is free, open-source and available to all.

* **Conda packages** from public channels such as **conda-forge**, **bioconda** or any other community channel, are free, open-source and available to all.

*  **Conda packages managed by Anaconda Inc.** and **Anaconda distribution** are free if and only if:
    - your organization has fewer than 200 employees, or
    - Your organization is exempt (e.g. students or educational institutions, provided it is used for program-based courses).

## How can I avoid licensed items?

* **Ban Anaconda Distribution**  
    Turn to other alternatives: Miniconda or preferably Miniforge. <[see here](./pages/conda-distrib)>  
    Install Miniforge <[see here](./pages/conda-installation)>

* **Ban [licensed channels](./pages/conda-channels/)**  
    Check and remove licensed channels in conda configuration. <[see here](./pages/conda-check)>  
    Prevent third parties from using licensed channels (when sharing environment). <[see here](./pages/conda-share)>  

This guide is designed to help you with these steps, and more. Enjoy your visit!