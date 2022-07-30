# Install Environment

## Clean Environment

Make sure that the following commands cause nothing to happen:
- `ipython`
- `python`
- `jupyter`

else delete those first

## Python

See Jeremy's "Live Coding 1" video here: https://www.youtube.com/watch?v=56sIyFjihEc&list=PLfYUBJiXbdtSLBPJ1GMx-sQWf6iNhb8mM&index=1
This avoids using the "system python" and allows to just delete the mambaforge directory and start over with a reinstall
Don't install python though apt-get or anything similar.  This is just for the system python.

- Locate installer for Mambaforge here: https://github.com/conda-forge/miniforge#mambaforge
- Download the installer: `wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh` 
- Run the script: `bash Mambaforge-Linux-x86_64.sh`
- Close and re-open the terminal
- it should prefix the path with (base)

This caused also the `.bashrc` in the homedirectory to be changed automatically so it starts with every shell.
We can see where python was installed by running `which python`

You have 3 options: pip, conda and mamba.  Conda and Mamba are fully compatible.  Mamba is newer.  Whenever you see "conda" you can replace that command with "mamba".  

## iPython

ipython is a Python REPL and can be installed through:
`mamba install ipython`

## Pytorch

Go to: https://pytorch.org/get-started/locally/
Choose the right options (pick "CUDA" if there's an NVIDEA GPU in the machine).
Run the command: `mamba install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch`

Also install the package "ipywidgets": `mamba install ipywidgets`

## Jupyter
We'll use Jupyter Lab.  See here: https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html
`mamba install -c conda-forge jupyterlab`

run Jupyter with: `jupyter lab`

## FastAI

`mamba install -c fastchan fastai`

## Fastbook

These are the dependencies needed for the FastAI notebooks.

`mamba install -c fastchan fastbook`
(Note that this includes FastAI)

## Sentencepiece

Needed in the NLP chapter for the FastAI course:

`mamba install -c fastchan sentencepiece`

## Fastbook

`git clone git@github.com:fastai/fastbook.git`

## GraphViz

`mamba install graphviz`
(Note that is could be this is already installed)