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


###### running notebooks from katmai

jupyter notebook command for some dinglab servers is weird, but the below should work for all nodes

First, run this on whatever node you are working on from within the cptac_driver conda environment. Replace PORT with whatever port you want (i.e. 12345, 11111, etc.), usually anything between 8000-50000 will work. Copy the link output by this command.
```bash
jupyter notebook --port PORT --no-browser --allow-root --ip=0.0.0.0
```

Then, on your machine run the following to connect the ports. Replace NODE_NAME with whatever node you are working on (i.e. acadia, sitka, etc.) and USERNAME with your username.

```bash
ssh -L PORT:NODE_NAME:PORT -N USERNAME@katmai.wusm.wustl.edu
```

Then past the link copied in the first step into your browser (make sure you replace NODE_NAME in that link with localhost) and everything should work :)
