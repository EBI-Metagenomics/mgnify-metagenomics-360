Opening the Jupyter notebook
----------------------------

|action| Open a new Terminal. There should be a Terminal application icon in the lefthand menubar.

|action| Type these commands to enter the repository:

.. code-block:: bash

    cd /home/training/genome-resolved-metagenomics-2022

    conda activate metagenomics

|info| That should have worked, but if you got an error you’ll need to create the environment:

.. code-block:: bash

    conda create --n metagenomics python=3.9

    conda activate metagenomics

    pip install -r requirements.txt

|action| To open the notebooks, run:

.. code-block:: bash

    jupyter-lab course.jupyterlab-workspace
    
|action| And follow the instructions to access the notebook using the Chromium browser
