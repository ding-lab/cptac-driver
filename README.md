## CPTAC driver pipeline

#### Install

First, download the repo

```bash
git clone https://github.com/ding-lab/cptac-driver.git
```

Then, create a conda environment from the environmental file within the repository and activate the conda environment.

```bash
cd cptac_driver
conda env create --file env.yaml
conda activate cptac_driver
```

#### Usage

First format input dataset with [format_model_inputs.ipynb](https://github.com/ding-lab/cptac-driver/blob/master/notebooks/format_model_inputs.ipynb)

Then, run pipeline with [modeling_pipeline.ipynb](https://github.com/ding-lab/cptac-driver/blob/master/notebooks/modeling_pipeline.ipynb)

Calculate driver scores with [calculate_driver_score.ipynb](https://github.com/ding-lab/cptac-driver/blob/master/notebooks/calculate_driver_score.ipynb)
