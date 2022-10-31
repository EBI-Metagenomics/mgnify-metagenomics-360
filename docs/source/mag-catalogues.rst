.. include:: partials/substitutions.rst

*************************
MGnify Genomes Catalogues
*************************

In the presentation we will cover:

- Recap of :ref:`mag:MAG Generation`
- Overview of MGnify MAG Catalogues
- Annotations available for catalogues and genomes
- Metadata available for catalogues and genomes
- Search mechanisms available against catalogues
- How MAG catalogues fit into the rest of the MGnify service

MAG Catalogues hands-on exercises
#################################

These exercises will again use the `API <https://en.wikipedia.org/wiki/API>`_ ("Application programming interface"),
showing how your scripts (e.g. Python or R) can talk to the MGnify database.

This builds on the exercises you looked at in the :ref:`services:API` practical.

The practical will use a Jupyter Notebook.

Fetch the code repository
-------------------------

.. code-block:: bash

    cd /home/training
    git clone https://github.com/EBI-Metagenomics/genome-resolved-metagenomics-2022.git

Do you have MAGs?
-----------------

|info| For the last few exercises, you need some MAGs.
If you didn’t get as far as making your own MAGs in the :ref:`mag:MAG Generation` exercises,
there should already be some in `/home/training/Binning/contigs.fasta.metabat-bins2000.bak`.

If you accidentally damaged those files, you can copy some from the shared drive:

.. code-block:: bash

    cp -r /media/penelopeprime/Metagenomics-Nov21/Day4/day-4-example-mag-bins/* /home/training/Binning/contigs.fasta.metabat-bins2000.bak/`

.. include:: partials/jupyter.rst

Today's Notebook is "Day 4".
