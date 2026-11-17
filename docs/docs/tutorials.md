# Tutorials

During the workshop, we will be running hands-on tutorials to demonstrate how to use NEMO Cookbook to analyse NEMO ocean model outputs, including hindcast simulations from the NOC Near-Present Day hierarchy.

For those with limited Python experience, we would recommend working through **Tutorial 0. Getting Started with xarray** prior to the hackathon to better understand the key data structures and operations used throughout the hackathon.

---

### **Pre-Event**

* **0. Getting Started with xarray**

    Ocean models produce large, multi-dimensional fields (e.g. temperature, salinity, velocity) that vary in time and space and are described by physical coordinates (e.g., depth). [**xarray**](https://docs.xarray.dev/en/stable/) provides data structures that explicitly represent these dimensions and coordinates, rather than treating model outputs as anonymous multi-dimensional arrays.

    This Jupyter Notebook provides an introduction to xarray for ocean model analysis and is intended as a quick reference that you can return to during the hackathon and beyond.

---

### **NEMO Cookbook Tutorials**

* **1. Getting Started with NEMO Cookbook.**

    In this Jupyter Notebook, we will demonstrate how to use the `NEMODataTree` object to analyse outputs of NEMO global ocean sea-ice simulations.

    We will cover:

    * Creating `NEMODataTree` objects directly from netCDF files and `xarray.Datasets`.

    * Opening virtual `NEMODataTrees` from Icechunk repositories.

    * Exploring NEMO model output variables stored in a `NEMODataTree`.

    * Geographical plotting of NEMO output variables.

    * Perform grid-aware operations using `NEMODataArrays`.
