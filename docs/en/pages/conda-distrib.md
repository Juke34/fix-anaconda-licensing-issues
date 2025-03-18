

|  | Anaconda | Miniconda (conda3-py312_24.9.2-0) | Miniforge (24.9.0-0) / Mambaforge | Micromamba | Pixi |
| -- | -- | -- | -- | -- | -- |
| Recommendation | **Ban** its use because it is licensed under anaconda and also uses channels licensed under anaconda. |  **Warning**, although it is free to use, you must configure its installation to avoid the `defaults` channel under anaconda license which is used by default. | **Best**. Free to use, and no licensed channel used by default. Be careful not to manually add licensed channels [see here](../conda-channels). |  **Best**. Free to use, and no licensed channel used by default. Be careful not to manually add licensed channels [see here](../conda-channels). | **Best**. Free to use, and no licensed channel used by default. Be careful not to manually add licensed channels [see here](../conda-channels) |
| Created and published by Anaconda | Yes | Yes | No | No | No |
| Contains conda | Yes | Yes | Yes | Yes (mamba) | No |
| Graphic interface | Yes | No | No | No | No |
| Number of preinstalled packages | 250+ | 72 | 74 | 0 | 0 |
| Installation space required | ~2 Gb | ~550 Mb | ~314 Mb | ~15 Mb | ~50 Mb
| Description | A complete distribution for data science, including Conda, Python, and around 300 popular libraries such as NumPy, pandas, and Jupyter, ready for use. | Minimal version of the Anaconda distribution, which installs only Conda, Python and their basic dependencies, without the Anaconda packages. | A minimal distribution similar to Miniconda, but configured to use conda-forge as the default channel. | Micromamba is a tiny version of the mamba package manager (C++ conda re-implementation). It is a statically linked executable with a separate command line interface. It does not need a base environment and does not come with a default version of Python. | Pixi is a project-centric package manager that builds upon the foundation of the conda ecosystem. Implemented in Rust, it is available as a single, statically linked file. It does not install a base environment. Its project-centric focus means each project has a separate environment.
| Disadvantages | Large size, paid license for companies with more than 200 employees. | By default, packages can be downloaded from Anaconda-licensed channels (defaults channel) | / | / | Not a drop-in replacement: Pixi has completely different CLI tool options.
