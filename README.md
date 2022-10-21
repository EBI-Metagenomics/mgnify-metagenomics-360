# Genome-resolved metagenomics course (Virtual) - 2022

Learn about the tools, processes and analysis approaches used in the field of metagenomics.

This course will cover the use of publicly available resources to manage, share, analyse and interpret metagenomics data; including marker gene, whole gene shotgun (WGS) and assembly-based approaches.

The virtually-delivered content will involve participants learning via pre-recorded lectures and live presentations, followed by live Q&As with the trainers. Practical experience will be developed in group activities and in computational exercises run in Docker containers on our virtual training infrastructure.

For more information about the course please refer to the [course page on the EBI Training website](https://www.ebi.ac.uk/training/events/metagenomics-bioinformatics-2022)

## Preparing the interactive notebooks

We will have to install the dependencies to run the notebooks. To do so, we will use [miniconda](https://docs.conda.io/en/latest/miniconda.html).

Open a Terminal.

```shell
(base) conda env create -n metagenomics -f environment.yml
(base) conda activate metagenomics

(metagenomics) pip install -r requirements.txt
(metagenomics) conda install -c conda-forge r-irkernel
(metagenomics) conda install -c conda-forge r-tidyverse
(metagenomics) conda install -c conda-forge r-devtools
(metagenomics) conda install ipykernel
(metagenomics) R
```

```R
> devtools::install_github("beadyallen/MGnifyR")
> install.packages("tidyverse")
> quit()
```

```shell
(metagenomics) jupyter-lab course.jupyterlab-workspace
```

Jupyter should be using the "metagenomics" kernel, so that the packages are available.
To check, look at the top right of the Jupyter Lab window:
![selecting kernel in jupyter](notebooks/assets/jupyter-kernel-selection.png)
