# Lab: Spatial Python with Jupyter Notebooks
## Worth: 50
## Due: 7 days
## Assignment

## Background
We previously worked with python within the framework of QGIS as well as the IDE. In this lab we are going to interact with python in what is called a Jupyter Notebook. Jupyter Notebooks are interactive apps set up for reproducible analysis and data science and are great for sharing methods with real examples. We are going to continue with geospatial python, showing an example with `fiona` as well as exploring `geopandas`, `rasterio`, and `rasterstats`.


Reference:
- [Jupyter Notebooks](https://jupyter.org/)
- [GeoPandas](http://geopandas.org/)
- [RasterIO](https://rasterio.readthedocs.io/en/stable/)
- [Rasterstats](https://pythonhosted.org/rasterstats/)

## Directions
### Setup Conda Environment
There are some additional steps to follow to allow Jupyter to recognize your anaconda environment. Open your Anaconda Shell and activate your `python37` environment, then use `ipykernel` to install the virtual environment connection with Jupyter. 

```
conda activate python37
conda install --yes pip
conda install --yes ipykernel
python -m ipykernel install --user --name python37 --display-name "Python (3.7)"
```

### Open Jupyter Navigator
In Jupyter Navigator, click on Environments. You should see the `python37` environment. Select it so that you get a green triangle indicating it is active, then go back to `Home`.

### Install Jupyter Notebook
Click on `Install` under the Jupyter Notebook icon. If you are prompted for an admin password and you don't have access, just click `Cancel`. It should still install.

### Launch Jupyter Notebook
See [https://jupyter.readthedocs.io/en/latest/running.html#running](https://jupyter.readthedocs.io/en/latest/running.html#running) for details about running `Jupyter`. When you run launch jupyter you are actually running a server and will connect to it through the browser. From the browser you can create a new notebook or load a new one.

Go ahead and click `Launch` from `Anaconda Navigator`. When you launch Jupyter Notebook it will open a browser window with a file listing, likely pointed at your home directory. If you are using GitHub Desktop, you can navigate to the directory where you have cloned this repo to by opening `Documents` -> `GitHub Desktop` -> `(this repo)`. You will see a list of files, some of which are Jupyter Notebooks with a `.ipynb` file suffix.


### Deliverabls



### Jupyter keyboard shortcuts
https://towardsdatascience.com/jypyter-notebook-shortcuts-bf0101a98330

jupyter labextension install @jupyter-widgets/jupyterlab-manager
