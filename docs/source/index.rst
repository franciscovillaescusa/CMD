.. CAMELS Multifield Challenge documentation master file, created by
   sphinx-quickstart on Sat Jun  5 20:05:31 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

CAMELS Multifield Dataset (CMD)
=================================

CMD is a publicly available collection of hundreds of thousands 2D maps and 3D grids containing different properties of the gas, dark matter, and stars from more than 2,000 different universes. The data has been generated from thousands of state-of-the-art (magneto-)hydrodynamic and gravity-only N-body simulations from the CAMELS project.

.. figure:: movie.gif

   Examples of 2D maps from CMD. From top-left to bottom right: gas temperature, gas pression, neutral hydrogen mass, electron number, metallicity, gas mass, dark matter mass, total mass, stellar mass, magnetic fields, magnesium over iron, gas velocity, and dark matter velocity. Each map is characterized by the value of the cosmological parameters (:math:`\Omega_{\rm m}` and :math:`\sigma_8`) and the astrophysical parameters (:math:`A_{\rm SN1}`, :math:`A_{\rm SN2}`, :math:`A_{\rm AGN1}`, and :math:`A_{\rm AGN2}`).

Each 2D map and 3D grid has a set of labels, or parameters, associated to it. Understanding the relation between the data and the labels will help cosmologists to decipher the misteries of our own Universe.
   
.. toctree::
   :maxdepth: 2
   :caption: Data

   description
   data

.. toctree::
   :maxdepth: 3
   :caption: Applications

   inference
   emulator
   mapping
   superresolution
   time_evolution

   
.. toctree::
   :maxdepth: 2
   :caption: Other

   science
   terminology
   publications
   citation
   license
   help
