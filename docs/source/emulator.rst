Emulators
=========

Since each 2D map and 3D grid is characterized by a set of 6 parameters, one natural application of CMD is to build emulators, i.e.

.. math::

   \textbf{X}=f(\vec{\theta})

where :math:`\textbf{X}` can be a summary statistics (e.g. the probability distribution function of the pixels in a 2D map), or can be the entire 2D map or 3D grid, :math:`\vec{\theta}` is a vector with the value of the parameters (e.g. :math:`\vec{\theta}=\{\Omega_{\rm m}, \sigma_8, A_{\rm SN1}, A_{\rm SN2}, A_{\rm AGN1}, A_{\rm AGN2} \}`) and :math:`f` is the function relating the parameters to the data.

The idea is to use neural networks or other methods to approximate :math:`f`. CMD provides a significant amount of data to achieve this task.
