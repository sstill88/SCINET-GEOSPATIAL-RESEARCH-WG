---
title: Tutorials
nav: true
---

All the tutorials are hosted at _______. Below is a brief description of each tutorial as well as an instructional on how to download and run them on the SCINet HPC Ceres.

{% capture text %}
* **Tutorials on Ceres 1**: How to Access/Run the tutorials on Ceres
* **Tutorial 1**: Getting onto SCINet
* **Tutorial 2**: Getting onto SCINet
* **Tutorial 3**: Getting onto SCINet
* **Tutorial 4**: Getting onto SCINet
{% endcapture %}
{% include card.md header="Overview" text=text %}

## Run Tutorials on SCINet/Ceres

To run the tutorials (excluding the *Getting Started* tutorial) follow the below instructions:

1. Log onto JupyterHub
   * Go to www.wakjshf;aljdf.gov
   * Fill out Spawning Page with the following:
     ```
     cores: asdfadf
     partition:  asdfasdf
     container: asdfasdf
     etc...
     ```

2. Download the Material
   * Open the terminal File-->New-->terminal
   * Download the tutorials
      ```bash
      git clone --single-branch https://github.com/kerriegeil/SCINET-GEOSPATIAL-RESEARCH-WG.git
      ```
3. Run a notebook:
   * You should now see a folder (file system extension on the left hand side of JuputerLab) titled *SCINET-GEOSPATIAL-RESEARCH-WG*.
   * Navigate to ```/SCINET-GEOSPATIAL-RESEARCH-WG/tutorials/```
   * Open the desired tutorial
   * Select the py_geo kernel (upper right in the notebook)
   * Execute blocks of script.

## Tutorial 2: _____

This tutorial teaches things....

## Tutorial 3: _____

This tutorial teaches things....

## Tutorial 4: Machine Learning with Harmonized Landsat Sentinel

### 4a: Machine Learning Intro

This tutorial briefly shows a subset of standard machine learning operations using a raster scene from the Harmonized Landsat Sentinel data. This tutorial does not require the computational capacity of SCINet, and can be executed on pesonal computing systems. This tutorial includes:

1. Read in data into a spatially aware object (Xarray).
2. Preprocess, shuffle, and split into training and testing data (Scikit Learn).
3. Train a model and optimize the hyperparameters (Scikit Learn).
4. Quantify the accuracy and visualize the results (Scikit Learn, hvPlot).

### 4b: Machine Learning - Distributed Learning on SCINet / Ceres

This tutorial uses machine learning, daily weather data (PRISM), physiologic variables (soil properties and topography) to predict NDVI from the Harmonized Landsat Sentinel (HLS) data at the Central Plains Experimental Range (CPER) Long Term Agro-ecosystem Research station. This workflow involves:

1. Read data into a consistent projection (Xarray).
2. Setup a cluster on Ceres (Dask Distributed)
3. Setup a pipeline to merge/shuffle/split the data, optimize the hyperparameters, and train an XGBoost model (Scikit Learn, XGBoost, Dask).
4. Quantify the accuracy and visualize the results (Scikit Learn, hvPlot).

The data is stored in a [zarr](https://zarr.readthedocs.io/en/stable/) file format. The analysis is conducted in Python with the following packages:

   * Dask - Distributed Computing
   * Xarray - Multidimensional data arrays
   * Sci-Kit Learn - Machine Learning
   * XGBoost - Xtreme Gradient Boosting
   * hvPlot - Interactive visualization library.

A Jupyter notebook of the anlaysis on the github page (link: [Machine Learning Example]()). In addition a link to the static (non-interactive) version of the notebook.