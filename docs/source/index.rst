.. CAMELS Multifield Challenge documentation master file, created by
   sphinx-quickstart on Sat Jun  5 20:05:31 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

CAMELS Multifield Challenge (CMC)
=================================

Cosmologists have developed a theoretical framework (the standard model of Cosmology) that is able to explain a very large variety of cosmological observations. This model has some free parameters that characterize fundamental properties of the Universe, such as its age, geometry, composition...etc.

One of the main goals of modern cosmology is to determine the value of these parameters with the highest accuracy. For this, the community has invested billions of dollars


The data from upcoming cosmological surveys may allow us to answer some of the most profounds questions in cosmology: What is the nature of dark energy? What is the absolute mass and hierarchy of neutrinos? How fast is the Universe expanding?

The main obstacle to accomplish this is not the quantity or quaility of the data, but the theoretical prediction needed to extract the relevant information from the data. Two difficult problems need to be overcomed: 1) the optimal summary statistic(s) needed to extract the maximum information from non-Gaussian density fields is unknown, and 2) the impact of astrophysical processes such as supernova and AGN feedback is poorly known.

In `Villaescusa-Navarro et al. 2020b  <https://arxiv.org/abs/2011.05992>`_ we showed using toy examples that neural networks can find optimal estimators that allows to extract the maximum cosmological information while marginalizing over baryonic effects. 

The CAMELS Multifield Challenge (CMC) provides a set of hundreds of thousands of 2-dimensional maps from 15 different fields of the state-of-the-art (magneto-)hydrodynamic simulations CAMELS as data to train machine learning algorithms, or traditional summary statistics, with the aim to extract the maximum cosmological information from them.

All data is publicly available together with the model and weights of the convolutional neural networks trained in `Villaescusa-Navarro et al. 2021a <>`_ that can be seen as the benchmark. 


.. toctree::
   :maxdepth: 2
   :caption: Introduction

   summary
	     
.. toctree::
   :maxdepth: 2
   :caption: Description

   science
   goals
   data
   description_maps
   description_benckmark
   
.. toctree::
   :maxdepth: 2
   :caption: Other

   terminology
   publications
   citation
   license
   help
