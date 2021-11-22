Download
========

CMD data can be downloaded in two different ways:

#. Via `globus <https://app.globus.org/file-manager?origin_id=1910cb10-4ba8-11ec-a516-b537d6c07c1d&origin_path=%2F>`_.
#. Via  `url  <https://users.flatironinstitute.org/~fvillaescusa/priv/DEPnzxoWlaTQ6CjrXqsm0vYi8L7Jy/CMD>`_.

.. Note::
  
   Transfering the data with the url is simple and convenient, but it can also be slow and unstable, in particular for the large files. We thus recommend using globus as it is the fastest and more reliable way to transfer the data.

Structure
---------

CMD data is organized as follows:

- **2D\_maps**. This folder contains 2 subfolders:
  
  - **data**. It hosts all files with the 2D maps and the values of the cosmological and astrophysical parameters.

  - **inference**. It hosts the codes and network weights used to perform parameter inference with CMD.

    
- **3D\_grids**. This folder only contains 1 subfolder:

  - **data**. All files with the 3D grids and the values of the cosmological and astrophysical parameters are here.

The total data volume of the 2D maps is approximate 100GB, and of the 3D grids is of 75TB.

The image below shows a scheme with the way the data is organized:
    
.. image:: Diagram.png
   :width: 600
   :align: center
