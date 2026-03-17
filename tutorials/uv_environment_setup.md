You can use your own machine or Google Colab, for now most of the exercises will use only small datasets. That said, we need a Python environment. There are many options, but we recommend `uv`:

https://docs.astral.sh/uv/concepts/projects/init/#applications

the following instructions will help you setup an environment that can be used in Jupyter notebooks or scripting. We also recommend using VS Code for implementing projects.

To begin with `uv`, check it is installed on your machine (you may need to install `pip`, see https://pip.pypa.io/en/stable/installation/)

pip install uv

uv init odsl_block_26 # Start a basic project (in the current dir) and virtual environment named "odsl_block_26"

uv pin python 3.12 # tell uv to use later version of python 

uv sync # this updates the project environment (it will automatically synchronise packages to be consistent with this python version)

uv add jax numpy matplotlib ipykernel scipy torch # install these packages, consistently with e.g. python3.12

uv sync # again update the environment

uv run python some_script.py # command line usage