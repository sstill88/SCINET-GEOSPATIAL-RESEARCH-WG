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

## Tutorials on Ceres

To run the tutorials (excluding the *logging into Ceres* tutorial) follow the below instructions:

1. Log onto JupyterHub
   * Go to www.wakjshf;aljdf.gov
   * Fill out Spawn like:<br>
     cores:<br> 
     partition:<br>
     container:kjhdsfa<br>
2. Download the Material
   * Open the terminal File-->New-->terminal
   * Download the tutorials by cloning the github repository.
      ```bash
      git clone _________.git
      ```
3. Run a notebook:
   * Browse to one of the tutorials and open it.
   * Select the py_geo kernel
   * Execute blocks of script

```bash
import numpy as np
import pandas as pd
import dask
```


## Tutorial 2: _____

This tutorial teaches things....

## Tutorial 3: _____

This tutorial teaches things....

```python
import numpy as np
import pandas as pd
import dask
```

## Tutorial 4: _____

This tutorial teaches things....

```python
import numpy as np
import pandas as pd
import dask
```
