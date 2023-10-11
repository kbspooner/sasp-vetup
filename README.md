sasp_vetup
==========

A collection of scripts written over time for myself, but perhaps the
reader will find something interesting :shrug:
Split into two directories, ``src``, which contains scripts designed to
be run directly from the command line, and ``tools``, which contains
scripts designed to be copied to the working directory, modified and
kept for posterity. Most of the former will accept ``-h`` or ``--help``
for more information, but I've listed some highlights below.

ptgrep
------

One of the simplest and most useful scripts, greps any number of
elements (well, up to 118 for now) from the periodic table.

potpunch
--------

Writes a ``POTCAR`` from a ``POSCAR`` file, using the recommended
``POTCAR``s as defaults. You must specify the POTCAR locations within
the script.

jwrite
------

Writes job files and more importantly auto-populates array job arrays,
as well as reads by-computer defaults set in the script by exporting a
``computer`` environment variable.

phonon-job
----------

Fire-and-forget job script for running large numbers of calculations in
parallel. DO NOT USE if you don't know what its doing (for everything
but especially this). You probably want to disable things like
``minimise-vasprun``.

input.yaml
----------

Various scripts take input.yaml files to autofill some data, such as
converged ``ENCUT`` values. Subdictionaries can also be used to override
these values, e.g. a higher ``ENCUT`` value for electronic structure
calculations.

convergence scripts
-------------------

Several scripts automate convergence, however I would recommend soon-to-
be-Dr. (and quickly thereafter Prof.) Sean Kavanagh's
[vaspup2.0](<https://github.com/kavanase/vaspup2.0) instead.

Installation
------------

The good ol' ``chmod u+x <file>`` and add it to your path.
