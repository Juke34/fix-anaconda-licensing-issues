

|  | Anaconda | Miniconda (conda3-py312_24.9.2-0) | Miniforge (24.9.0-0) / Micromamba / Mambaforge|
| -- | -- | -- | -- | 
| Recommendation | **Ban** its use because it is licensed under anaconda and also uses channels licensed under anaconda. |  **Warning**, although it is free to use, you must configure its installation to avoid the `defaults` channel under anaconda license which is used by default. | **Best**. Free to use, and no licensed channel used by default. Be careful not to manually add licensed channels [see here](../conda-channels). |
| Created and published by Anaconda | Yes | Yes | No |
| Contains conda | Yes | Yes | Yes | Yes | Yes
| Graphic interface | Yes | No | No |
| Number of preinstalled packages | 250+ | 72 | 74 |
| Installation space required | ~2 Gb | ~550 Mb | ~314 Mb |
| Description | A complete distribution for data science, including Conda, Python, and around 300 popular libraries such as NumPy, pandas, and Jupyter, ready for use. | Minimal version of the Anaconda distribution, which installs only Conda, Python and their basic dependencies, without the Anaconda packages. | A minimal distribution similar to Miniconda, but configured to use conda-forge as the default channel.
| Disadvantages | Large size, paid license for companies with more than 200 employees. | By default, packages can be downloaded from Anaconda-licensed channels (defaults channel) | / |
