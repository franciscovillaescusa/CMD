Description
===========

Simulations
-----------

CMD has been generated from thousands of state-of-the-art (magneto-)hydrodynamic and gravity-only N-body simulations from the `CAMELS project <https://www.camel-simulations.org>`__. CMD data can be classified into three groups, that indicate the type of simulation used to create the data:

- **IllustrisTNG**. These magneto-hydrodynamic simulations follow the evolution of gas, dark matter, stars, and black-holes. They also simulate magnetic fields. CMD uses 1,000 of these simulations. 

- **SIMBA**. These hydrodynamic simulations follow the evolution of gas, dark matter, stars, and black-holes. CMD uses 1,000 of these simulations. 
  
- **N-body**. These gravity-only N-body simulation only follow the evolution of dark matter. Thus, they do not model astrophysical processes such as the formation of stars and the feedback from black-holes. CMD uses 1,000 of these simulations. 

Structure
---------

CMD provides the following data generated from the above simulations:

**IllustrisTNG**

- 15,000 2D maps per field for 13 different fields. 195,000 2D maps in total.
- 15,000 3D grids per field for 13 different fields. 195,000 3D grids in total.
  
**SIMBA**

- 15,000 2D maps per field for 12 different fields. 180,000 2D maps in total.
- 15,000 3D grids per field for 12 different fields. 180,000 3D grids in total.

**Nbody**

- 15,000 2D maps of one single field. 15,000 2D maps in total.
- 1,000 3D grids of one single field. 1,000 3D grids in total.

The following table provides more details on the CMD structure:

+-----------------------+--------+--------------------+--------------------+--------------------+
| Field                 | Prefix | IllustrisTNG       | SIMBA              | Nbody              | 
+=======================+========+=========+==========+=========+==========+=========+==========+
|                       |        | 2D maps | 3D grids | 2D maps | 3D grids | 2D maps | 3D grids |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Gas mass              | Mgas   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Gas velocity          | Vgas   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Gas temperature       | T      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Gas pressure          | P      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Gas metallicity       | Z      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Neutral hydrogen mass | HI     | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Electron number       | ne     | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Magnetic fields       | B      | 15,000  | 15,000   | --      | --       | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Magnesium over Iron   | MgFe   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Dark matter mass      | Mcdm   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Dark matter velocity  | Vcdm   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Stellar mass          | Mstar  | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Total matter mass     | Mtot   | 15,000  | 15,000   | 15,000  | 15,000   | 15,000  | 15,000   |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
+-----------------------+--------+---------+----------+---------+----------+---------+----------+
| Total                 |        | 195,000 | 195,000  | 180,000 | 180,000  | 15,000  | 15,000   |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+


.. Note::
  
   All 2D maps have :math:`256^2` pixels and cover a periodic area of :math:`(25~h^{-1}{\rm Mpc})^2` at redshift 0. The 3D grids contain :math:`128^3`, :math:`256^3` or :math:`512^3` voxels over a volume of :math:`(25~h^{-1}{\rm Mpc})^3` and are at redshifts 0, 0.5, 1, 1.5, and 2. 

We show an example of how the IllustrisTNG images look like for the different fields:

.. image:: multifield.png

where from top-left to bottom-right: gas mass, gas velocity, gas temperature, gas pressure, dark matter mass, dark matter velocity, electron abundance, magnetic fields, stellar mass, neutral hydrogen gas metallicity, and magnesium over iron ratio.

These images show different properties of the gas, dark matter, and stars in a given Universe. Determining the value of the cosmological parameters from these images will help us to decode the true value of our own Universe, allowing us to unveil some of the biggest misteries in fundamental physics.

Labels
------

Each 2D map and 3D grid has a set of labels attached to it:

- :math:`\Omega_{\rm m}`. This is a cosmological parameter that represents the fraction of matter in the Universe.
- :math:`\sigma_8`. This is a cosmological parameter that controls the smoothness of the distribution of matter in the Universe.
- :math:`A_{\rm SN1}` and :math:`A_{\rm SN2}`. These are two astrophysical parameters that controls two properties of supernova feedback.
- :math:`A_{\rm AGN1}` and :math:`A_{\rm AGN2}`. These are two astrophysical parameters that control two properties of black-hole feedback.

The data from the IllustrisTNG and SIMBA simulations are described by all the above parameters, while the 2D maps and 3D grids generated from the N-body simulations are only characterized by the cosmological parameters :math:`\Omega_{\rm m}` and :math:`\sigma_8`.
  

2D maps
-------

The generic name of the files containing the maps is ``Images_prefix_sim_LH_z=0.00.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be IllustrisTNG, SIMBA or Nbody. For instance, the file containing the gas mass maps of the IllustrisTNG simulations is ``Images_Mgas_IllustrisTNG_LH_z=0.00.npy``. The 2D maps are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA gas temperature maps do:

.. code:: python

   import numpy as np

   # name of the file
   fmaps = 'Images_T_SIMBA_LH_z=0.00.npy'

   # read the data
   maps = np.load(fmaps)

The file contains 15,000 maps with :math:`256\times256` pixels each.

The value of the cosmological and astrophysical parameters characterizing the maps of a given field is ``params_sim.txt`` where ``sim`` can be IllustrisTNG, SIMBA or Nbody. These files can be read as this:

.. code:: python

   import numpy as np

   # name of the file
   fparams = 'params_SIMBA.txt'

   # read the data
   params = np.loadtxt(fparams)

The file contains 1,000 entries with 6 values per entry. The first and second entry are the value of :math:`\Omega_{\rm m}` and :math:`\sigma_8`, while the rest represent the value of the astrophysical parameters: :math:`A_{\rm SN1}`, :math:`A_{\rm AGN1}`, :math:`A_{\rm SN2}`, :math:`A_{\rm AGN2}`.

.. note::

   In the case of the ``Nbody`` maps, only the first and second columns (the ones containing the value of :math:`\Omega_{\rm m}` and :math:`\sigma_8`) are relevant. The other 4 columns can be disregarded. They are only kept to standarize the training of the networks.

The value of the cosmological and astrophysical parameters of a given map can be found as

.. code:: python

   map_number = 765
   params_map = params[map_number//15]


See this `colab <https://colab.research.google.com/drive/1bT1OXxEPi2IaFs7sJn96M7scFtiKLygj?usp=sharing>`_ for further details on how to manipulate the images and the value of the parameters.


3D grids
--------

The generic name of the files containing the 3D grids is ``Grids_prefix_sim_LH_grid_z=redshift.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be IllustrisTNG, SIMBA or Nbody, ``grid`` can be 128, 256, or 512 and ``redshift`` can be 0, 0.5, 1 or 1.5. For instance, the file containing the 3D gas metallicity of the IllustrisTNG simulations on a grid with ``256^3`` voxels at redshift 0 is ``Grid_Z_IllustrisTNG_LH_256_z=0.00.npy``. The 3D grids are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA neutral hydrogen mass at redshift 1.0 with a grid of ``128^3`` voxels do:

.. code:: python

   import numpy as np

   # name of the file
   fgrids = 'Grid_HI_SIMBA_LH_128_z=0.00.npy'

   # read the data
   grids = np.load(grids)

The file contains 1,000 grid with :math:`128\times128\times128` voxels each.

The value of the cosmological and astrophysical parameters characterizing the maps of a given field is ``params_sim.txt`` where ``sim`` can be IllustrisTNG, SIMBA or Nbody. These files can be read as this:

.. code:: python

   import numpy as np

   # name of the file
   fparams = 'params_SIMBA.txt'

   # read the data
   params = np.loadtxt(fparams)

The file contains 1,000 entries with 6 values per entry. The first and second entry are the value of :math:`\Omega_{\rm m}` and :math:`\sigma_8`, while the rest represent the value of the astrophysical parameters: :math:`A_{\rm SN1}`, :math:`A_{\rm AGN1}`, :math:`A_{\rm SN2}`, :math:`A_{\rm AGN2}`.

.. note::

   In the case of the ``Nbody`` maps, only the first and second columns (the ones containing the value of :math:`\Omega_{\rm m}` and :math:`\sigma_8`) are relevant. The other 4 columns can be disregarded. They are only kept to standarize the training of the networks.

The value of the cosmological and astrophysical parameters of a given grid can be found as

.. code:: python

   grid_number = 821
   params_map  = params[map_number]

   
Symmetries
----------

Each 2D map and 3D grid from CMD has a set of labels associated to it: two cosmological parameters and four astrophysical parameters (only in the case of data from IllustrisTNG and SIMBA simulations). These labels will remain the same if

- rotations
- translations
- parity

transformations are applied to the data.

Another important thing to take into account is that the data is periodic in all dimensions. For instance, in the case of 2D maps

.. code:: python

   import numpy as np

   # name of the file
   fmaps = 'Images_HI_IllustrisTNG_LH_z=0.00.npy'

   # read the data
   maps_HI = np.load(fmaps)

   # take the map number 36
   map_HI = maps_HI[36]

   # the pixel map_HI[45,89] is adjacent to the pixel map_HI[46,89]
   # the pixel map_HI[145,99] is adjacent to the pixel map_HI[145,98]
   # the pixel map_HI[76,0] is adjancent to the pixel map_HI[76,255]
   # the pixel map_HI[255,12] is adjancent to the pixel map_HI[0,12]


.. Note::

   When using convolutional neural networks, one can take advantage of this property by using periodic padding.
  
   
Disk space
----------
