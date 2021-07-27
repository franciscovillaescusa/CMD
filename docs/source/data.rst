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

The generic name of the files containing the maps is ``Images_prefix_sim_LH_z=0.00.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be IllustrisTNG, SIMBA or Nbody. For instance, the file containing the gas mass maps of the IllustrisTNG simulations is ``Images_Mgas_IllustrisTNG_LH_z=0.00.npy``. The 2D maps are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA gas temperature maps do:

.. code:: python

   import numpy as np

   # name of the file
   fmaps = 'Images_T_SIMBA_LH_z=0.00.npy'

   # read the data
   maps = np.load(fmaps)

The file contains 15,000 maps with :math:`256\times256` pixels each.

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

The generic name of the files containing the 3D grids is ``Grids_prefix_sim_LH_grid_z=redshift.npy``, where ``prefix`` is the word identifying each field (see table above), ``sim`` can be IllustrisTNG, SIMBA or Nbody, ``grid`` can be 128, 256, or 512 and ``redshift`` can be 0, 0.5, 1 or 1.5. For instance, the file containing the 3D gas metallicity of the IllustrisTNG simulations on a grid with ``256^3`` voxels at redshift 0 is ``Grids_Z_IllustrisTNG_LH_256_z=0.00.npy``. The 3D grids are stored as ``.npy`` files, and can be read with the numpy ``load`` routine. For instance, to read the SIMBA neutral hydrogen mass at redshift 1.0 with a grid of ``128^3`` voxels do:

.. code:: python

   import numpy as np

   # name of the file
   fgrids = 'Grids_HI_SIMBA_LH_128_z=0.00.npy'

   # read the data
   grids = np.load(fgrids)

The file contains 1,000 grids with :math:`128\times128\times128` voxels each. For large files (e.g. those containing the grids with :math:`512^3` voxels) it is better to read the files in a slightly different way, to avoid running out of RAM memory:

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
  
   
Storage
-------

Each pixel of a 2D map and each voxel of a 3D grid is stored as a float, i.e. it occupies 4 bytes.

A single 2D map that has :math:`256^2` pixels will take :math:`256^2\times4=0.25` Mb. CMD is organized into files that contain 15,000 maps per field. Those files require 3.75 Gb. Since there are 26 of those files in CMD (13 for IllustrisTNG, 12 for SIMBA, and 1 for N-body), downloading all 2D maps from CMD requires 97.5 Gb.

A single 3G grid with :math:`N^3` voxels will take :math:`N^3\times4` bytes, i.e. 8 Mb for :math:`N=128`, 64 Mb for :math:`N=256`, or 512 Mb for :math:`N=512`. CMD is organized into files that contain 1,000 3D grids for each field. Each of those files will occupy 7.8 Gb (:math:`N=128`), 62.5 Gb (:math:`N=256`), and 500 Gb (:math:`N=512`). All CMD files containing 3D grids at a given resolution and redshift will take 203.13 Gb, 1.59 Tb, and 12.7 Tb for :math:`N=128, 256, 512`, respectively. All files at all redshifts and resolutions will take 72.4 Tb.


