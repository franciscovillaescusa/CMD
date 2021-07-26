N-body to hydro
===============

For a fixed volume, mass, and spatial resolution, running (magneto-)hydrodynamic simulations is much more computationally expensive than running a gravity-only N-body simulations. 

This is a significant limitation and the reason why even today, we cannot run hydrodynamic simulations over scales of billions of ligh years, the ones that would be needed to analyze data from cosmological surveys. On the other hand, N-body simulations can be run over such large volumes with enough resolution.

One possible way around this is to learn how to paint gas and stars into the dark matter field simulated by N-body simulations. This way, we could simulate the result of a full (magneto-)hydrodynamic simulation from the output of a computationally cheap N-body simulation.

.. Note::

   This mapping can be done for a fixed cosmological and astrophysical model or can be done as a function of cosmology and astrophysics using CMD labels.
