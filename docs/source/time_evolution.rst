Time evolution
==============

Cosmological simulations typically start at high redshift (early cosmic times) and finish at redshift z=0 (present time). Several snapshots at different cosmic times are stored before the simulation finishes, and are used to post-process the data and to analyze the results of the simulation. In general, the more snapshots that can be saved, the better! On the other hand, each snapshot occupies disk space, so in practice, a limited number of snapshots can be saved.

Similar to the emulation task, it would be desirable to develop a method that takes as input a set of snapshots at some cosmic times and returns new snapshots at different times. This way, the main limitation associated with this problem will be fixed as snapshots can easily be produced a-posteriori.

CMD provides a rich dataset with plenty of data at different cosmic times for N-body and state-of-the-art (magneto-)hydrodynamic simulations.

.. Note::

   `2012.05472 <https://arxiv.org/abs/2012.05472>`__ carried out this task using N-body simulations. 



