# atsc5040-fair
Demonstration of how to run the FaIR simple energy balance model (https://docs.fairmodel.net/en/latest/index.html) for ATSC 5040. 

## Setup Steps:
Before running this notebook, you need to have the necessary Python packages installed. There are two options for this:
1. **(Recommended) Install the packages into a [conda](https://anaconda.org/anaconda/conda) virtual environment**: create a new conda environment with all the packages you will need using `conda env create -f environment.yaml`. When it is finished installing, run `conda activate atsc5040-fair-env` to activate the new envrionment.
3. **Install the packages directly using pip**: You will need [pandas](https://pandas.pydata.org/docs/getting_started/install.html), [xarray](https://docs.xarray.dev/en/latest/getting-started-guide/installing.html), [scipy](https://scipy.org/install/), and [fair](https://docs.fairmodel.net/en/latest/install.html). Run the following commands from your terminal:
    * `pip install pandas` (this needs to be installed before xarray if using pip)
    * `python -m pip install xarray`
    * `pip install scipy`
    * `pip install fair`

## Running the Model
TODO: describe basic process

## Contents of this Repository
Table of contents

## References
TODO - Fair publication, document links, etc. 
