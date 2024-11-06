![](pages/images/Conda_logo.jpg){: style="height:100px"}

# Avoiding the Pitfalls of the Anaconda License: A Practical Guide

Anaconda's license changes during 2024 have caused some concern, particularly in specific sectors such as academia, research and non-profit organizations, which have relied on the platform thinking it was available for free.

To complicate matters, there is often a misunderstanding of what is and isn't free when using conda, the package manager, versus the channels and distributions provided by Anaconda.

## What has changed?

The heart of the changes lies in Anaconda's definition of “Organizational Use”. Under the new [license conditions](https://legal.anaconda.com/policies/en/?name=terms-of-service#anaconda-terms-of-service), any organization (government entities and non-profit organizations) with at least 200 employees or contractors is now required to purchase a paid license to use Anaconda software or packages from Anaconda-managed channels.

## In brief

* **Conda**, the package manager, is free, open-source and available to all.

* **Conda packages** from public channels such as **conda-forge**, **bioconda** or any other community channel, are free, open-source and available to all.

*  **Conda packages managed by Anaconda Inc.** and **Anaconda distribution** are free if and only if:
    - your organization has fewer than 200 employees, or
    - Your organization is exempt (e.g. students or educational institutions, provided it is used for program-based courses).

## My organization has more than 200 employees, how can I avoid licensed items?

* **Ban Anaconda Distribution**  
    Turn to other alternatives: Miniconda or preferably Miniforge. <[see here](./pages/conda-distrib)>  
    Install Miniforge <[see here](./pages/conda-installation)>

* **Ban [licensed channels](./pages/conda-channels/)**  
    Check and remove licensed channels in conda configuration. <[see here](./pages/conda-check)>  
    Prevent third parties from using licensed channels (when sharing environment). <[see here](./pages/conda-share)>  

This guide is designed to help you with these steps, and more. Enjoy your visit!