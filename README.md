# Lab: Spatial Python with Jupyter Notebooks
## Worth: 50
## Due: 7 days
## Assignment

## Deliverable
`Pull request` to merge a new branch named `assignment` with `master`. Your branch should contain:
1. `screencap-hello.png`
2. `screencap-california-housing.png`
3. `screencap-streetlights.png`
4. `screencap-wards.png`

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
conda create -n python37 python=3.7
conda activate python37
conda install --yes -c conda-forge jupyter requests scipy numpy pandas  matplotlib descartes geopandas rasterstats  rasterio 
```

### Launch Jupyter Notebook
In the `python37` environment in Anaconda Shell:
```
jupyter notebook
```
This will open your default browser and a file listing will be displayed. Jupyter Notebook is a server application running in your shell and the browser is the client. Navigate to the directory where you have checked out this repository. This is likely going to be `Documents` -> `GitHub` -> `jupyter-notebooks-intro` or similar.

### Example Notebooks
Open and follow the notebooks, creating screenshots of the final map product in each one. 
1. hello.iphynb (save screenshot as `screencap-hello.png`)
2. California Housing.ipynb (save screenshot as `screencap-california-housing.png`)
3. streetlights-assignment.ipynb (save screenshot as `screencap-streetlights.png`)

### Copy `streetlights-assignment.ipynb` and use it as the basis for a new notebook
Copy the `streetlights-assignment.ipynb` notebook to a new one called `wards-barricades.ipynb` which will be a 
modification of the streetlights assignment. The background for this:

Your uncle now lives in Tucson and just experienced his first monsoon. He was not impressed with how the road
barricades were handled for urban flooding events and wants to discuss this with city representatives. But before
he meets with the city council he wants to find out how many barricades there are in each district. Luckily, the
City of Tucson makes the water barricade data available on their Open GIS Data Portal. Your final product will be a map
of wards with a choropleth symbology based on the number of barricades in each ward.

#### Data
- http://gisdata.tucsonaz.gov/datasets/operation-splash-open-data (Points)
- http://gisdata.tucsonaz.gov/datasets/city-of-tucson-wards-open-data (Polygon)

#### Hints
The workflow is very similar to the streetlights notebook but you will not need to create a heatmap. In fact, this
is simply a spatial join between the polygons and the points. What you want is "number of barricades by ward"

Remember that `geopandas.sjoin(point, poly)` will give a new attribute to the points table with the attributes of the polygon it intersects. That's step 1. Once you have that attribute, you will want to use the pandas `.groupby()` function. That will give you a table of the counts of points by ward. The final step is to join _that_ table back to the wards themselves using the pandas `.merge()` function. 

Relevant docs:
- [Geopandas `sjoin`](http://geopandas.org/reference/geopandas.sjoin.html)
- [Pandas `groupby`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.core.groupby.GroupBy.count.html)
- [Pandas `merge`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.merge.html#pandas.DataFrame.merge)

4. Take a screenshot of your final map product and name it `screencap-wards.png`

### _Helpful: Jupyter keyboard shortcuts_
https://towardsdatascience.com/jypyter-notebook-shortcuts-bf0101a98330
