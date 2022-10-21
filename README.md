# Woberdepop
Wat handige scriptjes voor het downloaden van WOB verzoeken en het analyseren van je twitter feeds. 

In de folder `wob-download` vind je een paar jupyter notebooks.

Als je zelf aan de slag wilt :`download-wob-documenten.ipynb` is je startpunt.

Dan pdf vertalen naar txt met de `pdf2txt.ipynb`.

Daarna `topic-model.ipynb` hierin wordt de hele corpus gelezen en opgeschoont. Ook worden er wat filters over de txt heenb gehaalt, inclusief stopwoorden. Er worden ook wat tussen resultaten weggeschreven die je in de volgende notebooks als startpunt kunt gebruiken.

De andere notebooks gaan er van uit dat je die tussen resultaten beschikbaar hebt.

Het 'word2vec.ipynb' notebook maakt een word embedding die je kunt vertalen naar een fomaat voor de [embedding projector](https://projector.tensorflow.org/) van tensorflow.

Als je de embedding hebt opgeslagen kun je met het volgende commando de file voor de projector genereren:

    python -m gensim.scripts.word2vec2tensor -i wob_word2vec.model -o ./projector


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
