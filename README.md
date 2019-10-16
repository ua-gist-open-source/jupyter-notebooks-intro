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
conda install --yes -c conda-forge jupyter rasterstats requests scipy rasterio numpy pandas geopandas matplotlib descartes proj4==5.2.0
```

### Launch Jupyter Notebook
In the `python37` environment in Anaconda Shell:
```
jupyter notebook
```
This will open your default browser and a file listing will be displayed. Jupyter Notebook is a server application running in your shell and the browser is the client. Navigate to the directory where you have checked out this repository. This is likely going to be `Documents` -> `GitHub` -> `jupyter-notebooks-intro` or similar.

### Open and follow/execute the code in the three notebooks:
_Look ahead to deliverables to find out what to save_
1. hello.iphynb
2. California Housing.ipynb
3. streetlights-assignment.ipynb

### Create a new notebook

### _Helpful: Jupyter keyboard shortcuts_
https://towardsdatascience.com/jypyter-notebook-shortcuts-bf0101a98330

## Deliverables:
Submit the following in a new branch with a pull request to merge with `master` of this repo:

From `California Housing.ipynb`:
1. Screenshot of final map

From `streetlights-assignment.ipnyb`:
1. Screenshot of `light_avg` map 
2. Screenshot of chloropleth map of barricades by ward
3. Screenshot of table showing barricades by ward
