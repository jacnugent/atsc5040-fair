# atsc5040-fair
Demonstration of how to run the FaIR simple energy balance model (https://docs.fairmodel.net/en/latest/index.html) for ATSC 5040 at the University of Wyoming, Fall 2025. 

## Setup Steps

### 1. Clone the repository.
`git clone https://github.com/jacnugent/atsc5040-fair.git`

### 2. Install the python packages.
Before running this notebook, you need to have the necessary Python packages installed. Note that this can take several minutes. There are two options for this:
1. **(HIGHLY recommended!) Install the packages into a [conda](https://anaconda.org/anaconda/conda) virtual environment**: create a new conda environment with all the packages you will need using `conda env create -f environment.yaml`. When it is finished installing, run `conda activate atsc5040-fair-env` to activate the new envrionment.
2. **Install the packages directly using pip**: You will need [Jupyter](https://jupyter.org/install), [pandas](https://pandas.pydata.org/docs/getting_started/install.html), [xarray](https://docs.xarray.dev/en/latest/getting-started-guide/installing.html), [scipy](https://scipy.org/install/), [fair](https://docs.fairmodel.net/en/latest/install.html), and [matplotlib](https://matplotlib.org/stable/install/index.html). Run the following commands from your terminal:
    * `pip install jupyter`
    * `pip install pandas` (this needs to be installed before xarray if using pip)
    * `python -m pip install xarray`
    * `pip install scipy`
    * `pip install fair`
    * `python -m pip install -U matplotlib`
  
### 3. Check your setup.
Run the command `jupyter notebook` to launch Jupyter, and then run **`test_setup.ipynb`**. This notebook should run without errors if the setup completed properly. 

## Running the Model
See the notebook **`fair_demo.ipynb`** for a basic tutorial on how to run FaIR.

## Contents of this Repository
* **files/**: Input data files necessary to run the notebook. Includes ERF files for various SSPs (`ERF_ssp*_1750-2500.csv`) and the CMIP6 model parameters file (`4xCO2_cummins_ebm3.csv`).
* **environment.yaml**: Environment file containing all the packages needed to run the notebook.
* **environment.yml**: ^Exact same file above, but with a different extension; this is needed to match the naming convention for [binder](https://2i2c.mybinder.org/).
* **test_setup.ipynb**: Basic, condensed noteook to test that the setup/package installation was successful.
* **fair_demo.ipynb**: Example notebook to run FaIR; _this is the meat of the demo_.

## References
* FaIR documentation: https://docs.fairmodel.net/en/latest/index.html
* ERF_ssp* files:
   * Smith, C. (2023): Chapter 7 of the Working Group I Contribution to the IPCC Sixth Assessment Report - data for Figure 7.SM.1 (v20220721). NERC EDS Centre for Environmental Data Analysis, 10 July 2023. doi:10.5285/f0f622f4e9d14f95949a5cc44451e8bb. https://dx.doi.org/10.5285/f0f622f4e9d14f95949a5cc44451e8bb
* FaIR publications:
   * Leach, N. J., Jenkins, S., Nicholls, Z., Smith, C. J., Lynch, J., Cain, M., Walsh, T., Wu, B., Tsutsui, J., and Allen, M. R.: FaIRv2.0.0: a generalized impulse response model for climate uncertainty and future scenario exploration, Geosci. Model Dev., 14, 3007--3036, https://doi.org/10.5194/gmd-14-3007-2021, 2021
   * Smith, C. J., Forster, P. M., Allen, M., Leach, N., Millar, R. J., Passerello, G. A., and Regayre, L. A.: FAIR v1.3: A simple emissions-based impulse response and carbon cycle model, Geosci. Model Dev., https://doi.org/10.5194/gmd-11-2273-2018, 2018.
