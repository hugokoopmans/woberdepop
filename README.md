# woberdepop
wat handige scriptjes


## Howto setup the python environment

Goto extracted folder

Create virtual environment with conda

    conda create --name wob

Source this environemnt

    conda activate wob

Add relevant libraries to the requirements.txt

Install requirements

    pip3 install -r requirements.txt

We need to make sure the jupyter notebook server sees this new environment.

Make all kernels installed on conda available to jupyter

    conda install nb_conda_kernels
    
And the notebook extentions

    conda install -c conda-forge jupyter_contrib_nbextensions

Install the Jupyter Notebook

    conda install -c anaconda jupyter