<p align="left">
    <img src="./docs/docs/assets/icons/NEMO_Cookbook_Logo.png" alt="Logo" width="200" height="90">
</p>

## **NEMO Cookbook Tutorial**

**Last Updated: 17/11/2026**

:book: [**Tutorial Documentation**](https://oj-tooth.github.io/nemo_cookbook_tutorial/)

## What is NEMO Cookbook? :cook: :book:
NEMO Cookbook extends the familiar xarray data model with grid-aware data structures designed for performing reproducible analyses of the Nucleus for European Modelling of the Ocean ([**NEMO**](https://www.nemo-ocean.eu)) ocean general circulation model outputs.

Our aim is to provide a collection of recipes implementing the post-processing & analysis functions available in [**CDFTOOLS**](https://github.com/meom-group/CDFTOOLS) alongside new diagnostics (e.g., surface-forced water mass transformation), which are compatible with generalised vertical coordinate systems (e.g., MES).

Each recipe uses the `NEMODataTree` and `NEMODataArray` structures to leverage [**xarray**](https://xarray.dev), [**flox**](https://flox.readthedocs.io/en/latest/) & [**dask**](https://www.dask.org) libraries (think of these are your cooking utensils) to calculate a diagnostic with NEMO ocean model outputs (i.e., the raw ingredients - that's where you come in!).

---

## Getting Started :hammer:

To participate in our hands-on tutorial sessions and get started exploring the outputs of the NOC Near-Present Day simulations, follow the instructions below to install NEMO Cookbook in a new virtual environment and download a local copy of the tutorial materials. 

### Downloading Tutorials

Let's start by making a local copy of the `nemo_cookbook_tutorial` GitHub repository including the Jupyter Notebook tutorials.

Navigate to your chosen working directory, and then clone the GitHub repo:

```bash
git clone https://github.com/oj-tooth/nemo_cookbook_tutorial.git
```

Once the download is complete, you will see that a new `NEMO_cookbook_tutorial` directory has been added to your working directory.

Inside the `nemo_cookbook_tutorial` directory, you will find:

* `/docs` - Documentation source files for the [**NEMO Cookbook Tutorial website**](https://oj-tooth.github.io/nemo_cookbook_tutorial/)

* `/tutorials` - Jupyter Notebooks for NEMO Cookbook Tutorials

> **Note:** Editing any of the tutorial or example notebooks / creating new notebooks in your cloned `nemo_cookbook_tutorial` will not impact the original GitHub repository.

### Creating a New Virtual Environment

If you do not already have an installation of miniconda, miniforge or pixi on your local machine, see the instructions below on how to install miniforge, otherwise proceed to 

**Installing Miniforge**

Miniforge is a minimal conda installer that defaults to the **conda-forge** ecosystem. It is lightweight, open-source, and recommended for scientific Python workflows.

To download Miniforge, follow instructions at [**https://github.com/conda-forge/miniforge**](https://github.com/conda-forge/miniforge).

For Unix-like Platforms (macOS, Linux, WSL): 

```bash
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

**Creating the Base Environment**

Run the installer by running the following command:

```bash
bash Miniforge3-$(uname)-$(uname -m).sh
```

It is recommended to accept the default location (`~/miniforge3`) and only accept the changes to your `~/bashrc` file if you are happy for the base environment to be activated every time you log in (this is not recommended for JASMIN use).

**Activating the Base Environment**

Once you have successfully installed miniforge3, activate your base environment:

```bash
source ~/miniforge3/bin/activate 
```

### Adding NEMO Cookbook to your Virtual Environment

When we cloned the `nemo_cookbook_tutorial` GitHub repository, it included a `nemo_cookbook_environment.yml` file to install the Python packages needed to run the tutorial notebooks.

From your conda base environment, run the following command to create a new Python virtual environment and install NEMO Cookbook and its dependencies:

```bash
conda env create --name env_nemo --file nemo_cookook_environment.yml
```

This will take a bit of time to install all of the dependencies from the **conda-forge** channel and then **OceanDataStore** and **NEMO Cookbook** packages using `pip`.

For those who would prefer to install the latest release of **NEMO Cookbook** into an existing virtual environment, use the following command:

```bash
pip install nemo_cookbook
```

### Creating a New Jupyter Kernel [Optional]:

Once you have successfully created the `env_nemo` virtual environment, you can optionally set-up a Jupyter Kernel - the computational engine for your Python code - if you intend to use Jupyter Hub / Jupyter Lab.

To install a Jupyter kernel for your `env_nemo` conda environment, you first need to activate your `env_nemo` environment from the base environment using:

```bash
conda activate env_nemo
```

Then, run the following command to add a new Jupyter kernel called env_nemo to your kernelspec:

```bash
python -m ipykernel install --user --name env_nemo --display-name "NEMO Cookbook Tutorial (env_nemo)"
```

Now, when you open a notebook in Jupyter Lab, you will see a **Select Kernel** drop-down menu and included in the list is `NEMO Cookbook Tutorial (env_nemo)` kernel.


## Resources

Below we have provided a list of useful links to documentation and resources to support those with limited experience of the **xarray**, **flox** or **OceanDataStore** libraries used in the tutorials.

* **xarray Tutorial**

    [**https://tutorial.xarray.dev/intro.html**](https://tutorial.xarray.dev/intro.html)

* **Flox**

    [**https://flox.readthedocs.io/en/latest/**](https://flox.readthedocs.io/en/latest/)

* **Earth & Environmental Data Science Book**

    [**https://earth-env-data-science.github.io/intro.html**](https://earth-env-data-science.github.io/intro.html)

* **Cosima Cookbook**

    [**https://cosima-recipes.readthedocs.io/en/latest/**](https://cosima-recipes.readthedocs.io/en/latest/)

* **NOC Near-Present Day**

    [**https://noc-msm.github.io/NOC_Near_Present_Day/**](https://noc-msm.github.io/NOC_Near_Present_Day/)

* **OceanDataStore**

    [**https://noc-msm.github.io/OceanDataStore/**](https://noc-msm.github.io/OceanDataStore/)

* **NEMO Cookbook**

    [**https://noc-msm.github.io/nemo_cookbook/**](https://noc-msm.github.io/nemo_cookbook/)


## **Contributors**

- **Ollie Tooth** (oliver.tooth@noc.ac.uk)
- **Adam Blaker** (atb299@noc.ac.uk)
- **Andrew Coward** (acc@noc.ac.uk)

## **Funding**

The ongoing development of NEMO Cookbook is funded by the following projects: 

- **AtlantiS**: [Atlantic Climate and Environment Strategic Science](https://atlantis.ac.uk)
- **ARIA - PROMOTE**: [Progressing earth system Modelling for Tipping Point Early warning systems](https://aria.org.uk/opportunity-spaces/scoping-our-planet/forecasting-tipping-points/)
- **EPOC**: [Explaining & Predicting the Ocean Conveyor](https://epoc-eu.org)
