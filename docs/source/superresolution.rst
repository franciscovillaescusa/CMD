Superresolution
===============

Cosmological simulations can be run at different mass and spatial resolutions. For a fixed volume, the higher the mass and spatial resolution the more computationally expensive the simulation will be. This is a major bottleneck for current numerical simulations. One possible way around this is to run a low resolution simulation and increase its resolution a-posteriori using some sophisticated method.

CMD provides for each field and redshift three different 3D grids of the same spatial distribution for N-body simulations but also for (magneto-)hydrodynamic simulations. That data can be used to train and test superresolution methods that can tackle this important challenge.

.. warning::

   We note that the three different sets of grids available in CMD have different spatial resolution but the simulations used to create them have the same mass resolution. Previous works have changed both mass and spatial resolution in data from N-body simulations: `2001.05519 <https://arxiv.org/abs/2001.05519>`__, `2010.06608 <https://arxiv.org/abs/2010.06608>`__, `2105.01016 <https://arxiv.org/abs/2105.01016>`__. 
