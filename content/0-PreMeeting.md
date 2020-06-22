---
title: Premeeting
nav: true
--- 

Please review the workshop schedule and pre-meeting tasks listed below.

{% capture text %}
1. Have SCINet credentials.
2. Attend the "Premeeting" event if you need help accessing Ceres.
3. Review the tutorials - know which ones you wish the attend.
4. Familiarize yourself with the software.
{% endcapture %}
{% include card.md text=text header="PreMeeting Checklist" %}

------
## Tutorials

The tutorials span the range of beginner (new to SCINet/Ceres) to more advanced (Big Data and Machine Learning). If you have questions about the material, please do not hesitate to contact the organizing committee.

In general, these tutorials assume some level of knowledge in scientific programming.

------
## Ceres Access

SCINet credentialing process: [https://scinet.usda.gov/guide/quickstart](https://scinet.usda.gov/guide/quickstart)

Access JupyterHub (with SCINet credentials): [https://jupyterhub.scinet.usda.gov/](https://jupyterhub.scinet.usda.gov/)

If you have issues accessing Ceres (either thru SSH or JupyterHub) please attend the premeeting event (see the schedule) where the Virtual Research Support Core (VRSC) will be able to help trouble shoot any issues.

------
## Software + Hardware + Nomenclature Overview

The software discussed and shown in the workshop is largely open source, can run on a dekstop, HPC, or cloud environment, and can be installed with software management systems that support reproducibility (such as conda, singularity, and docker). Below is a quick overview of some of the software, hardware, and confusing nomenclature that will be used during this workshop.

**SCINet vs. Ceres**

SCINet is an USDA ARS initiative to improve access to high performance and cloud computing, increase networking to facilitate high speed data transfer, and to facilitate scientific computing training.

Ceres is the HPC system housed at Iowa State University. It contains 2500 compute cores, 27 TB RAM, 150 TB local storage, and 2.4 PB of shared storage.

**Project Jupyter**

Jupyter is an open-source, non-profit project to support interactive data science and scientific computing. Jupyter is language agnostic with support for >130 different scinetific programing language kernels. This workshop will use the following two applications from the Jupyter software stack:
  1. JupyterHub: A software to serve JupyterLab to multiple users (this is how we will launch an instance of JupyterLab on Ceres without having to to SSH into the cluster). Documention at: [https://jupyterhub.readthedocs.io/en/stable/](https://jupyterhub.readthedocs.io/en/stable/)
  2. JupyterLab: A web-based interactive development environment. Documentation at: [https://jupyterlab.readthedocs.io/en/stable/](https://jupyterlab.readthedocs.io/en/stable/)

**Slurm**

[Slurm](https://slurm.schedmd.com/quickstart.html) is the cluster management software used on Ceres to allocate computational resources.

**Scientific Coding Languages - Python and R**

The tutorials in this workshop will use Python, but we will make an effort to discuss alternative approaches in R. Python and R appear to be the most common scientific programming languages used across ARS. We choose to focus on Python simply due to instructor expertise. However, many of these examples could also be run in other programming languages such as Julia, Go, IDL/ENVI, etc...

**Containers and Environments**

Environments are a method of isolating a set of software installed on a computing system. In this workshop we will largely be discussing environments in the context of the [anaconda (conda)](https://www.anaconda.com/products/individual) software stack. However, other software management systems impliment similiar approaches.

Containers are a unit of isolated software that include an entire runtime environment (applications, dependencies, libraries, and binaries). These systems were created to be able to reliably run computing environments across hetereogenous infrastructure. The container system used on Ceres (and most other HPC systems) is [singularity](https://sylabs.io/docs/). However, singularity is able to use containers from Docker, a much more prevalent containerization software.

The use of both containers and environments can vastly improve the reproduciblity of computatoinal research. Environments are able to acheive this by keeping a detailed list of the exact software environment used for the computation. Containers are able to further this effort by essentially archiving/saving the exact environment in a "*container file*", which others can access and use on other systems.

**GitHub**

GitHub is a Git (version controll software) repository hosting service. Much of the workshops materials will be accessible thru the workshops GitHub repository at: [https://github.com/kerriegeil/SCINET-GEOSPATIAL-RESEARCH-WG](https://github.com/kerriegeil/SCINET-GEOSPATIAL-RESEARCH-WG). GitHub allows you to version and/or archive your code.