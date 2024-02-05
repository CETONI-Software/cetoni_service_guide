.. include:: include/colors.rst

.. role:: sg-yellow-bg
.. role:: sg-green-bg  
.. role:: sg-blue-bg
.. role:: sg-pink-bg


Qmix P / Q+ / Q- / TC and V Modules
===================================

Edit device parameters - Overview
---------------------------------

To edit the device paramaters of the above mentioned Qmix devices you
can use the QmixElements CANopenTools Plugin. 

.. rst-class:: steps

#. To open the CANopenTools
   Plugin, start the QmixElements software and select from the main menu
   the menu item :menuselection:`Device -> Open Configuration`.

   .. image:: media/image62.png

#. Then select the :menuselection:`canopentools (shared)` configuration:

   .. image:: media/image63.png

#. Connect your Qmix module to you BASE module and turn it on. Then click
   the :guilabel:`Connect` :guinum:`❶` button in the QmixElements software and scan for connected
   devices :guinum:`❷`.

   .. image:: media/image64.png

#. The software should detect the connected module :guinum:`❶`. Click with the right
   mouse button on the entry with the detected device and select :guilabel:`Assign EDS File` 
   :guinum:`❷` (see figure below).

   .. image:: media/image65.png

#. Select the valid EDS file :file:`ChipF40.eds` for the Qmix module from the
   existing EDS-files.

   .. image:: media/image66.png

#. You can now access all device and configuration parameters of the
   device:

   .. image:: media/image67.png

.. admonition:: Attention
   :class: caution

   Changing device parameters can cause             
   malfunctions or cancel safety mechanisms. Only change       
   device parameters as instructed by the technical support    
   staff.    