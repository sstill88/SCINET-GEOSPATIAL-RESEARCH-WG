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
   * Download the tutorials by cloning the github repository.
      ```bash
      git clone _________.git
      ```
3. Run a notebook:
   * You should now see a folder (file system extension on the left hand side of JuputerLab). Move into folder titled XXXXXXXXX.
   * Open the desired tutorial
   * Select the py_geo kernel (upper left in the notebook)
   * Execute blocks of script.


## Tutorial 2: _____

This tutorial teaches things....

## Tutorial 3: _____

This tutorial teaches things....

## Tutorial 4: _____

This tutorial teaches things....

```python
import numpy as np
import pandas as pd
import dask
```
