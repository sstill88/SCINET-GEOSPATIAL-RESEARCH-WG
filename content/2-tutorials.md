---
title: Tutorials
nav: true
---

All the tutorials are hosted at _______. Below is a brief description of each tutorial as well as an instructional on how to download and run them on the SCINet HPC Ceres.

{% capture text %}
* **Run Tutorials on Ceres**: How to Access/Run the tutorials on Ceres
* **Tutorial 1**: Intro to Ceres
* **Tutorial 2**: Parallel and Distrubuted Computing (Python)
* **Tutorial 3**: Developing Reproducible Research (Environments and Containers)
* **Tutorial 4**: Machine Learning (Python)
{% endcapture %}
{% include card.md header="Overview" text=text %}

## Run Tutorials on Ceres

To run the tutorials on Ceres (excluding the *Intro to Ceres* and *Developing Reproducible Research* tutorials) follow the below instructions:

1. Log onto JupyterHub
   * Go to [https://jupyterhub.scinet.science](https://jupyterhub.scinet.science/)
   * Log into the system with your SCINet credentials
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

## Tutorial 1: Intro to Ceres

This tutorial teaches things....

## Tutorial 2: Parallel and Distrubuted Computing (Python)

This tutorial teaches things....

## Tutorial 3: Developing Reproducible Research

This tutorial teaches things....

## Tutorial 4: Machine Learning with Harmonized Landsat Sentinel

This tutorial uses a machine learning model (XGBoost) to predict NDVI (Harmonized Landsat Sentinel) from daily weather (PRISM) and physiologic variables (soil properties) at the Central Plains Experimental Range (CPER) Long Term Agro-ecosystem Research station. This workflow involves:

1. Setup a cluster on Ceres (Dask Distributed).
2. Read data and interpolate onto a consistent grid (Xarray, Dask Dataframe).
3. Merge/shuffle/split the data (Dask_ML, Scikit Learn).
4. Optimize the hyperparameters (Dask_ML, Scikit Learn, XGBoost).
5. Train a distributed XGBoost model (Scikit Learn, XGBoost, Dask_ML).
4. Quantify the accuracy and visualize the results (Scikit Learn, hvPlot, Shap).

Static Notebook: [Machine Learning Example - Not complete](Machine_Learning_Tutorial.html)<br>
Github Link:  
