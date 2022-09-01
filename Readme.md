# Introduction to GeoPandas and its Python ecosystem

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/martinfleis/opengeohub2022-tutorial/main?urlpath=lab/)

The ecosystem of packages for spatial data handling and analysis in Python is extensive
and covers both vector and raster analytics from small to large distributed data. This
talk will cover only a small part, focusing on vector data processing with GeoPandas at
its core. First, we will cover what GeoPandas is and how it relates to other packages
and combines them into a user-friendly API. Then we will look at what GeoPandas enables
with a light introduction to PySAL - Python Spatial Analysis Library for spatial
statistics and modelling. The final part will touch on the scalability issue and
introduce how to handle parallel computation and big data using GeoPandas and Dask. All
of that will be illustrated by hands-on tasks on real-world data.

## Setting up to follow the tutorial

### Step 1: download the tutorial material

If you are a git user, you can get the tutorial materials by cloning this repo:

```bash
git clone https://github.com/martinfleis/opengeohub2022-tutorial.git
cd opengeohub2022-tutorial
```

Otherwise, to download the repository to your local machine as a zip-file, click the
`download ZIP` on the repository page
<https://github.com/martinfleis/opengeohub2022-tutorial> (green button "Code"). After
the download, unzip on the location you prefer within your user account (e.g. `My
Documents`, not `C:\`).

### Step 2: install the required Python packages

To follow the tutorial, we recommend to create a `conda` environment to ensure you have
all the required packages installed (the [environment.yml](environment.yml) file list
the required packages).

If you do not yet have `conda` installed, you can install miniconda
(<https://conda.io/miniconda.html>) or the (larger) Anaconda distribution
(<https://www.anaconda.com/download/>).

Using conda, we recommend to create a new environment with all packages using the
following commands (after cloning or downloading this github repo and navigating to the
directory, see above):

```bash
# setting the configuation so all packages come from the conda-forge channel
conda config --add channels conda-forge
conda config --set channel_priority strict
# creating the environment
conda env create --file environment.yml
# activating the environment
conda activate geopandas-tutorial
```

In case you do not want to install everything and just want to try out the course
material, use the environment setup by Binder
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/martinfleis/opengeohub2022-tutorial/main?urlpath=lab/)
and open the notebooks right away.

### Step 3: starting Jupyter Lab

The tutorial itself is a [Jupyter notebook](http://jupyter.org/), an interactive
environment to write and run code.

In the terminal, navigate to the `opengeohub2022-tutorial` directory (downloaded or
cloned in the previous section)

Ensure that the correct environment is activated.

```bash
conda activate geopandas-tutorial
```

Start a jupyter notebook server by typing

```bash
jupyter lab
```

After finishing you can deactivate the environment with

```bash
conda deactivate
```

## Acknowledgements

This tutorial is more closely or more loosely based on the following resources:

- [Introduction to GeoPandas](https://geopandas.org/en/latest/getting_started/introduction.html) by Martin Fleischmann and GeoPandas contributors
- [GeoPandas API reference](https://geopandas.org/en/stable/docs/reference.html) by GeoPandas contributors
- [Getting started (pandas)](https://pandas.pydata.org/docs/getting_started/index.html) by Stijn Van Hoey and pandas contributors
- Arribas-Bel, (2019). A course on Geographic Data Science. Journal of Open Source Education, 2(14), 42, [https://doi.org/10.21105/jose.00042](https://doi.org/10.21105/jose.00042)
- Introduction to geospatial data analysis with GeoPandas and the PyData stack bu Joris van den Bossche (<https://github.com/jorisvandenbossche/geopandas-tutorial>)
- Fleischmann, M., Feliciotti, A. and Kerr, W. (2022), Evolution of Urban Patterns: Urban Morphology as an Open Reproducible Data Science. Geogr Anal, 54: 536-558. [https://doi.org/10.1111/gean.12302](https://doi.org/10.1111/gean.12302)
- datos.gob.es [Administrative province boundaries in Catalonia](https://datos.gob.es/en/catalogo/a09002970-limites-administativos-provinciales-de-catalunya)
