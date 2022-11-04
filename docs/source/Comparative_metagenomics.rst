.. include:: partials/substitutions.rst

*************************
Comparative metagenomics 
*************************

Normalization methods, alpha & beta diversity, and differentially abundant taxa
###############################################################################

In this practical session we aim to demonstrate how the MGnifyR tool can be used to fetch data and metadata of a MGnify metagenomic analyisis. With this data, we show how to generate diversity metrics for comparative metagenomics. Finally, we will run an analisys to detect differentially abundant taxa. The dataset is the TARA ocean metagenomic study (WMS) corresponding to size fractions for prokaryotes `MGYS00002008. <https://www.ebi.ac.uk/metagenomics/studies/MGYS00002008#overview>`_ Find more information about the `TARA Ocean Project. <https://fondationtaraocean.org/en/expedition/tara-oceans/>`_

The data we are using are abundance tables of taxonomic profiles gerated through the MGnify pipeline version 5.0.

|workflow|\

`MGnifyR <https://rdrr.io/github/beadyallen/MGnifyR/f/doc/MGnifyR.Rmd>`_ is a library that provides a set of tools for easily accessing and processing MGnify data in R, making queries to MGnify databases through the MGnify API. The benefit of MGnifyR is that data can either be fetched in tsv format or be directly combined in a phyloseq object to run an analysis in a custom workflow.

The excercises are organized in 4 main sections:

1. Fetching data and preprocessing (MGnifyR)
2. Normalization, alpha diversity indices and taxonomic profiles visualization (phyloseq)
3. Comparative metagenomics at community-level: Beta diversity (vegan)
4. Detection of differentially abundant taxa (SIAMCAT)


Comparative metagenomics hands-on exercises
###########################################

The practice has been prepared in a Jupyter Notebook available in the gihub repo.


Opening the Jupyter notebook
----------------------------

|action| Open a new Terminal and type these commands to clone and enter the repository:

.. code-block:: bash

    cd /home/training/ && mkdir comparative && cd comparative
    
    git clone https://github.com/EBI-Metagenomics/genome-resolved-metagenomics-2022.git

    cd genome-resolved-metagenomics-2022
    
    conda activate metagenomics
    
    jupyter-lab course.jupyterlab-workspace
    
    
|action| Find and open Comparative metagenomics notebook in the 'notebooks' directory 

|info| The notebook has colored boxes to indicate relevant steps in the analysis or to introduce material for discussion.

Yellow boxes:
	* Up to you: To re-run the analysis changing parametra
	* Questions: For open discussion

Blue boxes:
	* Notes: Informative boxes about the running command
	* Tips: Information useful for results interpretation

|info| To leave the notebook, you can save the changes and close the window. Type CTRL+C to terminate the process at the terminal.


.. |workflow| image:: media/assembly_mgnify.png
