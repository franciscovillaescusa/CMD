Parameter Inference
===================

One of the most obvious applications of CMD is parameter inference. CMD contains a collection of hundreds of thousands of 2D maps and 3D grids with different properties of the comic gas, dark matter, stars, and black holes from 2,000 different universes that span tens of light years apart. Each of those maps and grids is characterized by 6 numbers: two cosmological parameters describing fundamental properties of the Universe and four astrophysical parameters that quantify the efficiency of astrophysical processes supernova explosions or feedback from black holes. The task is to develop robust models that can infer the value of the two cosmological parameters from the data with the highest accuracy.


In this work and this work parameter inference from the 2D maps of CMD was carried out. Here we release all codes and network weights used in that analysis as a benchmark model to compare with.

Requisites
----------

- python3
- numpy
- `Pytorch <https://pytorch.org>`_
- `optuna <https://optuna.org>`_

Organization
------------

The folder containing the codes and weights is called ``benchmark``, and is located within the ``2D_maps`` folder. Inside it, there are three folders called ``scripts``, containing the codes used to train and test the networks, ``databases`` with the optuna databases and ``weights``, that has the weights of the networks.

scripts
-------

This folder contains the following codes:

- ``architecture.py``. This script contains different architecture models. 
- ``data.py``. This script process the data to train the networks.
- ``train.py``. This is the code used to train the network. 
- ``test.py``. This is the code used to test the network. 

To train a new model on a given field, or a multifield, follow these steps:

1) Open the code ``train.py`` and set the value of the different parameters in the INPUT section.
2) Run the code: ``python train.py``. Note that when using optuna, several trials can be run in parallel (see the optuna documentation for details).
3) The code will output an optuna database, and will save the losses and weights of each of the considered trials.

To test a model on a given field(s), or a multifield, follow these steps:

1) Open the code ``test.py`` and set the value of the different parameters in the INPUT section.
2) Run the code: ``python test.py``. 
3) The code will generate a file with true value of the parameters, together with the mean and standard deviation of the posterior for each parameter.

This `colab <https://colab.research.google.com/drive/1-BmkA8JSc36O8g9pj7FenD1YSLKqjQR3?usp=sharing>`__ shows an example on how to train and test a model using these scripts.
   
databases
---------

We use the optuna software to find the best value of the hyperparameters (learning rate, weight decay...etc) of one particular model. Typically, for each field, we perform 50 trials, where a trial corresponds to the training carried out with one particular choice of the value of the hyperparameters. This folder contains the databases created by optuna with the information about the different trials for the different simulation types.

The generic name of one of these files is ``sim_o3_field_all_steps_500_500_o3.db`` where ``sim`` can be IllustrisTNG, SIMBA, or Nbody, ``field`` is the considered field (can be several fields together). In some cases we smooth out the fields with a Gaussian kernel with width ``width`` (in pixel units). The generic name of these files is ``sim_o3_field_all_steps_500_500_o3_smoothing_width.db``.

These files can be read with optuna package, and two arguments are needed:

- ``study_name``. For all our databases, this variable is set to ``wd_dr_hidden_lr_o3``.
- ``storage``. This should be set to the a sqlite database with the name of the file, e.g. ``sqlite:////home/fvillaescusa/CMC/2D_maps/benchmark/databases/SIMBA_o3_HI_all_steps_500_500_o3.db``

We provide an example on how to read the information of these files in this `colab <https://colab.research.google.com/drive/1ab79y_nIr2JkkgtT_QJhjLTJYNjY9M0B?usp=sharing>`__.

.. Note::

   The databases files are very light (typically less than 1 Mb each), so they all can be downloaded easily. The files containing the network weights are however bigger (~100 Mb), so it may be a good idea to only download the weights for the best model or the top 5 models.


weights
-------

This folder contains the weights of all the models trained. Thus, for each field, there will be at least 50 different files containing the weights of the 50 different trials considered. The generic name of these files is ``weights_sim_field_trialnumber_all_steps_500_500_o3.pt``, where ``sim`` can be IllustrisTNG, SIMBA, or Nbody, ``field`` is the name of the considered field (can be several of them), and ``trialnumber`` is the trial number. In the cases where the neural network is trained on fields that are smoothed with a Gaussian kernel, the generic name of the files is ``weights_sim_field_trialnumber_all_steps_500_500_o3_smoothing_width.pt``, where width is the width of the Gaussian kernel in pixel units.

These files can be read by Pytorch routines once the architecture is specified. In all the cases, the architecture employed is ``o3_err`` (see ``architecture.py`` from the released codes). We provide an example on how to read these files in this `colab <https://colab.research.google.com/drive/18Bbwb30m1dqFccAZlUsJPNaH9iTNOibS?usp=sharing>`__.



challenges
----------

The results obtained with the above model were very promising. The network were able to determine the value of the cosmological parameters with a few percent accuracy. However, some problems raised up. The most important was that for some fields, the model was not robust. For instance, if the model was trained on 2D maps from the IllustrisTNG simulations, it worked ery well when tested on maps from those simulations, but it failed when tested on 2D maps from the SIMBA simulations.

We think the three main challenges for the parameter inference task are:

- Build models to infer the value of the cosmological parameters that are more accurate than the above benchmark.
- Build models that trained on one set of simulations (e.g. IllustrisTNG) can infer the correct cosmology when tested on the other set (e.g. SIMBA).
- Determine the minimum set of fields than contain 90% and 95% of the cosmological and astrophysical information.

Solving the above challenges will help cosmologists to extract the maximum robust information from cosmological surveys, unveiling the laws and constituents of our own Universe.
