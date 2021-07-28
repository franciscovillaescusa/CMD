Description
===========

Simulations
-----------

CMD has been generated from thousands of state-of-the-art (magneto-)hydrodynamic and gravity-only N-body simulations from the `CAMELS project <https://www.camel-simulations.org>`__. CMD data can be classified into three groups, that indicate the type of simulation used to create the data:

- **IllustrisTNG**. These magneto-hydrodynamic simulations follow the evolution of gas, dark matter, stars, and black-holes. They also simulate magnetic fields. CMD uses 1,000 of these simulations. 

- **SIMBA**. These hydrodynamic simulations follow the evolution of gas, dark matter, stars, and black-holes. CMD uses 1,000 of these simulations. 
  
- **N-body**. These gravity-only N-body simulation only follow the evolution of dark matter. Thus, they do not model astrophysical processes such as the formation of stars and the feedback from black-holes. There is an N-body simulation for each (magneto-)hydrodynamic simulation. CMD uses 2,000 of these simulations. 

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

- 30,000 2D maps of one single field. 30,000 2D maps in total.
- 2,000 3D grids of one single field. 30,000 3D grids in total.

The table below lists the 13 types of fields represented by the data and provides basic information about them.

+-----------------------+--------+--------------------+--------------------+--------------------+--------------------------------------+
| Field                 | Prefix | IllustrisTNG       | SIMBA              | Nbody              | Units                                |
+=======================+========+=========+==========+=========+==========+=========+==========+======================================+
|                       |        | 2D maps | 3D grids | 2D maps | 3D grids | 2D maps | 3D grids |                                      |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Gas mass              | Mgas   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`M_\odot/h`                    | 
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Gas velocity          | Vgas   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | km/s                                 |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Gas temperature       | T      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | Kelvin                               |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Gas pressure          | P      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`M_\odot{\rm (km/s)^2/kpc^3}`  |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Gas metallicity       | Z      | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | dimensionless                        |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Neutral hydrogen mass | HI     | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`M_\odot/h`                    | 
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Electron number       | ne     | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`1/h`                          |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Magnetic fields       | B      | 15,000  | 15,000   | --      | --       | --      | --       | Gauss                                |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Magnesium over Iron   | MgFe   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | dimensionless                        |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Dark matter mass      | Mcdm   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`M_\odot/h`                    | 
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Dark matter velocity  | Vcdm   | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | km/s                                 |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Stellar mass          | Mstar  | 15,000  | 15,000   | 15,000  | 15,000   | --      | --       | :math:`M_\odot/h`                    | 
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Total matter mass     | Mtot   | 15,000  | 15,000   | 15,000  | 15,000   | 30,000  | 30,000   | :math:`M_\odot/h`                    | 
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+
| Total                 |        | 195,000 | 195,000  | 180,000 | 180,000  | 30,000  | 30,000   |                                      |
+-----------------------+--------+---------+----------+---------+----------+---------+----------+--------------------------------------+

where :math:`M_\odot` represents the mass of the Sun, km/s stands for kilometers per second, :math:`h` is the reduced Hubble constant, that in all CMD is fixed to 0.67, and :math:`{\rm kpc}` stands for kiloparsec (3,260 light years).

.. Note::
  
   All 2D maps have :math:`256^2` pixels and cover a periodic area of :math:`(25~h^{-1}{\rm Mpc})^2` at redshift 0. The 3D grids contain :math:`128^3`, :math:`256^3` or :math:`512^3` voxels over a volume of :math:`(25~h^{-1}{\rm Mpc})^3` and are at redshifts 0, 0.5, 1, 1.5, and 2. 

We show an example of how the IllustrisTNG images look like for the different fields:

.. image:: multifield.png

where from top-left to bottom-right: gas mass, gas velocity, gas temperature, gas pressure, dark matter mass, dark matter velocity, electron abundance, magnetic fields, stellar mass, neutral hydrogen gas metallicity, and magnesium over iron ratio.

These images show different properties of the gas, dark matter, and stars in a given Universe. Determining the value of the cosmological parameters from these images will help us to decode the true value of our own Universe, allowing us to unveil some of the biggest mysteries in fundamental physics.

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

The generic name of the files containing the maps is ``Maps_prefix_sim_LH_z=0.00.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be ``IllustrisTNG``, ``SIMBA``, ``Nbody_IllustrisTNG``, or ``Nbody_SIMBA``.

.. Note::

   In the case of the Nbody data we add an extra word, ``IllustrisTNG`` or ``SIMBA``, to characterize the matching data from the (magneto-)hydrodynamics simulations. See :ref:`matching-data` for further details. 

For instance, the file containing the gas mass maps of the IllustrisTNG simulations is ``Maps_Mgas_IllustrisTNG_LH_z=0.00.npy``. The 2D maps are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA gas temperature maps do:

.. code:: python

   import numpy as np

   # name of the file
   fmaps = 'Maps_T_SIMBA_LH_z=0.00.npy'

   # read the data
   maps = np.load(fmaps)

The file contains 15,000 maps with :math:`256^2` pixels each.

We note that the name of the files for the Nbody 2D maps is slighty different to reflect the (magneto-)hydrodynamic simulation they should be matched on:

The values of the cosmological and astrophysical parameters characterizing the maps of a given field are given in ``params_sim.txt`` where ``sim`` can be IllustrisTNG, SIMBA or Nbody. These files can be read as follows:

.. code:: python

   import numpy as np

   # name of the file
   fparams = 'params_SIMBA.txt'

   # read the data
   params = np.loadtxt(fparams)

The file contains 1,000 entries with 6 values per entry. The first and second entries are the values of :math:`\Omega_{\rm m}` and :math:`\sigma_8`, while the rest represent the values of the astrophysical parameters: :math:`A_{\rm SN1}`, :math:`A_{\rm AGN1}`, :math:`A_{\rm SN2}`, :math:`A_{\rm AGN2}`.

.. note::

   In the case of the ``Nbody`` maps, only the first and second columns (the ones containing the values of :math:`\Omega_{\rm m}` and :math:`\sigma_8`) are relevant. The other 4 columns can be disregarded (because the Nbody simulations do not model supernovae and black holes). They are only kept to standardize the training of the networks.

The values of the cosmological and astrophysical parameters of a given map can be found as

.. code:: python

   map_number = 765
   params_map = params[map_number//15]


See this `colab <https://colab.research.google.com/drive/1bT1OXxEPi2IaFs7sJn96M7scFtiKLygj?usp=sharing>`_ for further details on how to manipulate the images and the values of the parameters.


3D grids
--------

The generic name of the files containing the 3D grids is ``Grids_prefix_sim_LH_grid_z=redshift.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be ``IllustrisTNG``, ``SIMBA``, ``Nbody_IllustrisTNG``, or ``Nbody_SIMBA``, ``grid`` can be ``128``, ``256``, or ``512`` and ``redshift`` can be 0, 0.5, 1, 1.5 or 2.

.. Note::

   In the case of the Nbody data we add an extra word, ``IllustrisTNG`` or ``SIMBA``, to characterize the matching data from the (magneto-)hydrodynamics simulations. See :ref:`matching-data` for further details. 

For instance, the file containing the 3D gas metallicity of the IllustrisTNG simulations on a grid with ``256^3`` voxels at redshift 0 is ``Grids_Z_IllustrisTNG_LH_256_z=0.00.npy``. The 3D grids are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA neutral hydrogen mass at redshift 1.0 with a grid of ``128^3`` voxels do:

.. code:: python

   import numpy as np

   # name of the file
   fgrids = 'Grids_HI_SIMBA_LH_128_z=0.00.npy'

   # read the data
   grids = np.load(fgrids)

The file contains 1,000 grids with :math:`128^3` voxels each. For large files (e.g. those containing the grids with :math:`512^3` voxels) it is better to read the files in a slightly different way, to avoid running out of RAM memory:

.. code:: python

   import numpy as np

   # name of the file
   fgrids = 'Grids_Mcdm_Nbody_LH_512_z=0.00.npy'

   # read the data
   grids = np.load(fgrids, mmap_mode='r')

   # take the first 3D grid
   grids[0]

   # multiply all the grids from numbers 672 to 700 by 3
   grids[672:700]*3

   

The values of the cosmological and astrophysical parameters characterizing the maps of a given field are given in ``params_sim.txt`` where ``sim`` can be IllustrisTNG, SIMBA or Nbody. These files can be read as follows:

.. code:: python

   import numpy as np

   # name of the file
   fparams = 'params_SIMBA.txt'

   # read the data
   params = np.loadtxt(fparams)

The file contains 1,000 entries with 6 values per entry. The first and second entries are the values of :math:`\Omega_{\rm m}` and :math:`\sigma_8`, while the rest represent the values of the astrophysical parameters: :math:`A_{\rm SN1}`, :math:`A_{\rm AGN1}`, :math:`A_{\rm SN2}`, :math:`A_{\rm AGN2}`.

.. note::

   In the case of the ``Nbody`` maps, only the first and second columns (the ones containing the values of :math:`\Omega_{\rm m}` and :math:`\sigma_8`) are relevant. The other 4 columns can be disregarded (because the Nbody simulations do not model supernovae and black holes). They are only kept to standardize the training of the networks.

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
   fmaps = 'Maps_HI_IllustrisTNG_LH_z=0.00.npy'

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

   
.. _matching-data:
   
Matching data
-------------

There are several ways to match CMD.

1. The 2D maps and 3D grids can be matched across fields within the same simulation type. For instance, the maps number 2786 of the files ``Maps_ne_IllustrisTNG_LH_z=0.0.npy`` and ``Maps_B_IllustrisTNG_LH_z=0.0.npy`` represent the same region of the same simulation. The only difference is that the first map will show the electron abundance while the second shows the magnetic fields. The same thing applies to the 3D grids. For instance, the grids number 621 of the files ``Grids_HI_SIMBA_LH_128_z=0.0.npy`` and ``Grids_Mgas_SIMBA_LH_128_z=0.0.npy`` represent the same volume of the same simulation with the only difference that the first grid shows the neutral hydrogen mass while the second contains the gas mass.

.. warning::

   This matching only applies to data within the same simulation. E.g. the files ``Maps_Mcdm_IllustrisTNG_LH_z=0.0.npy`` do not have any correspondence with the maps in the file ``Maps_Mtot_SIMBA_LH_z=0.0.npy``.

2. The 3D grids can be matched across resolution within the same field and redshift. For instance, the grids number 167 of the files ``Grids_Vcdm_SIMBA_LH_128_z=1.0.npy`` and ``Grids_Vcdm_SIMBA_LH_256_z=1.0.npy`` represent exactly the same field over the same volume with the only difference that the first contains :math:`128^3` voxels while the second has :math:`256^3` voxels. Knowing this mapping is important for the :ref:`superresolution` application.

3. The 2D maps and 3D grids can be matched between (magneto-)hydrodynamic and N-body simulations. For instance, the maps number 7413 of the files ``Maps_Mtot_IllustrisTNG_LH_z=0.0.npy`` and ``Maps_Mtot_Nbody_IllustrisTNG_LH_z=0.0.npy`` represent the same region of the same field (total matter), with the only difference that the first map was generated from an IllustrisTNG magneto-hydrodynamic simulation while the second one is from a gravity-only N-body simulation. Knowing this mapping is important to be able to quantify that impact of astrophysical processes on a given task.

.. warning::

   This mapping only applies to the total matter field.

4. The 3D grids can be matched across cosmic time in both the (magneto-)hydrodynamic and the N-body simulations. For instance, the grids number 923 ``Grids_Vgas_SIMBA_LH_512_z=0.0.npy`` and ``Grids_Vgas_SIMBA_LH_512_z=2.0.npy`` represent the gas velocity of the same universe just at two different times: :math:`z=0` in the first grid and :math:`z=2` in the second grid.

.. Note::

   We do not recommend using the above time matching for the 2D maps. The reason is that in a simulation, particles will move with time, so particles that are in a given map at a given time may move to another map at a different time. While this is not a problem for the 3D grids, it may be a challenge for the 2D maps.

We note that the above three matchings can be combined. For instance, in the :ref:`mapping` application we want to find the mapping between the total matter from an N-body simulation and a given field from a (magneto-)hydrodynamic simulation. In this case, the grids number 714 of the files ``Grids_T_SIMBA_LH_256_z=0.0.npy`` and ``Grids_Mtot_Nbody_SIMBA_LH_256_z=0.0.npy`` represent the same region at redshift 0, the first grid will contain the gas temperature from the hydrodynamic simulation while the second is the total matter field from the equivalent N-body simulation.
  
   
Storage
-------

Each pixel of a 2D map and each voxel of a 3D grid is stored as a float, i.e. it occupies 4 bytes.

A single 2D map that has :math:`256^2` pixels will take :math:`256^2\times4=0.25` Mb. CMD is organized into files that contain 15,000 maps per field. Those files require 3.75 Gb. Since there are 27 of those files in CMD (13 for IllustrisTNG, 12 for SIMBA, and 1+1 for N-body), downloading all 2D maps from CMD requires ~100 Gb.

A single 3G grid with :math:`N^3` voxels will take :math:`N^3\times4` bytes, i.e. 8 Mb for :math:`N=128`, 64 Mb for :math:`N=256`, or 512 Mb for :math:`N=512`. CMD is organized into files that contain 1,000 3D grids for each field. Each of those files will occupy 7.8 Gb (:math:`N=128`), 62.5 Gb (:math:`N=256`), and 500 Gb (:math:`N=512`). All CMD files containing 3D grids at a given resolution and redshift will take 211 Gb, 1.65 Tb, and 13.2 Tb for :math:`N=128, 256, 512`, respectively. All files at all redshifts and resolutions will take 75.2 Tb.


