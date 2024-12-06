# DCnet

Code accompanying the manuscript "Flexible Context-Driven Sensory Processing in Dynamical Vision Models"

## Initializing conda environment
To initialize conda environment, create an empty conda environment with Python 3.12 and pip installed
```
conda env create --name ei_rnn python=3.12 pip
```
Alternatively, you can create a conda environment from the `requirements/env.yaml` file in this repository (Note: there are some extra packages there that you may not need)
```
conda env create --file requirements/env.yaml --name ei_rnn
```
This file will create an environment that can be run on a linux machine with a CUDA-capable GPU running drivers compatible with CUDA 12.1 or higher. For other configurations, create the empty environment as above and follow the instructions below for installing the other dependencies.

## Installing required packages
To install the required packages for your system, activate your environment and pip isntall the file in `requirements/` that matches your system
```
conda activate ei_rnn
pip install -r requirements/<requirements_file>
```
where `<requirements_file>` should be replaced with `cu117.txt`, `cu121.txt`, `linux_cpu.txt`, `osx.txt` based on your system

## Running the code
To train the model, execute the following command in your active conda environment
```
python train.py <kwargs>
```
You should replace with `<kwargs>` with any parameters you wish to override. The defaults can be found in `config/config.yaml`. Leave this blank if you wish to use the defaults