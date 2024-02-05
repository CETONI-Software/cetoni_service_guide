.. include:: include/colors.rst

.. role:: sg-yellow-bg
.. role:: sg-green-bg  
.. role:: sg-blue-bg
.. role:: sg-pink-bg


Nemesys Service Tool
====================

Download
--------

For most service procedures in this guide you need special software –
the Nemesys Service Tool – **EPOS Studio**. You can download this service
tool from this location:

https://cetoni.com/software-downloads/


Installation
------------

.. rst-class:: steps

#. Run the downloaded :file:`*.exe` file to start the installation. 

#. Select the custom setup and ensure that the following components are selected
   (*EPOS*, *EPOS2* and *EPOS Studio*):

.. image:: media/image8.png


Start
-----
.. admonition:: Important
   :class: note

   Before you start the EPOS Studio make sure that your Starter Module /
   Base Module is properly connected to your PC and switched on. Make sure
   that no other pump is connected to your Starter Module and that only one
   Nemesys pump is connected to your Base Module.

.. admonition:: Important
   :class: note

   Only one single pump should be connected to your 
   PC when using the service tool to avoid communication       
   issues and to prevent accidental modification of device     
   parameters. 

Now start the EPOS Studio software. The Startup wizard appears and
guides you through the creation of an EPOS Studio project.

.. rst-class:: steps

#. Select :menuselection:`Create New Project`.

   .. image:: media/image9.png

#. Enter a project name.

   .. image:: media/image10.png

#. Skip this step.

   .. image:: media/image11.png

#. Select the communication driver :menuselection:`CANopen` :guinum:`❶` (or RS232, if you are
   connected via RS232) and add it to your drivers in the network on the
   right side :guinum:`❷`.

   .. image:: media/image12.png

#. Click the :guilabel:`Finish` button.

   .. image:: media/image13.png

#. Now you should see the applications screen.

   .. image:: media/image14.png


Searching for devices (nodes)
-----------------------------

.. rst-class:: steps

#. Right click on the **CAN0** communication interface and select 
   :guilabel:`Scanning Devices`.

   .. image:: media/image15.png

#. In the following Scanning Devices dialog, click the :guilabel:`Settings` button.

   .. image:: media/image16.png

#. In the Scanning Settings dialog, deselect all Transfer Rates **except
   1000000 Bit/s** :guinum:`❶`. Then deselect :guilabel:`LSS Method` :guinum:`❷` and click :guilabel:`OK` 
   :guinum:`❸`.

   .. image:: media/image17.png

#. Now click the :guilabel:`Start Scanning` Button in the Scanning Devices dialog. The
   software now tries to communicate with all devices starting from ID 1 to
   ID 127.

   .. image:: media/image18.png

#. As soon as a node appears in the list of scanned devices :guinum:`❶`, you can stop
   the scanning by clicking the :guilabel:`Stop Scanning` button :guinum:`❷`. Then close the
   Scanning Devices dialog by clicking the :guilabel:`OK` button in the bottom right.
   Now you should see the main application window again with the detected
   node below CAN0 interface:

   .. image:: media/image19.png

#. Click with the right mouse button on the node and then select
   :guilabel:`Connect` from the context menu.

   .. image:: media/image20.png

#. Now the red cross should disappear from the node item and you are
   connected to the device. It is possible that the device indicates a **CAN
   Passive Mode Error** right after connection in the status panel at the
   bottom (see figure below). This is not a real error but just an
   indication that no other device was connected to the bus at the time
   when the device was turned on.

   .. image:: media/image21.png

#. To clear this error, simply click with the right mouse button on the
   error message, and select the menu item :guilabel:`Clear All Entries` from the
   context menu (figure below).

   .. image:: media/image22.png

Now your device should be properly connected and you are ready to
proceed with further operations. The following picture shows, how your
communication panel should look like if everything went well.

.. image:: media/image23.png


Parameter export / import
-------------------------

Open parameter export/import wizard
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: media/image24.png

To start the parameter export/import wizard, click with the right mouse
button on the node you would like to configure. Then select the **Wizards**
from the context menu and in the Wizards menu select :guilabel:`Parameter Export / Import`.

Device Parameter Import
~~~~~~~~~~~~~~~~~~~~~~~

.. admonition:: Caution
   :class: error
  
   Before you import any parameters into your device, 
   you should export your current device parameters so that    
   you can restore them later in case something goes wrong     
   with the parameter import or in case you imported the wrong 
   parameters. 

.. rst-class:: steps

#. In the Parameter Export/Import dialog first click the :guilabel:`…` button 
   on the right to select a parameter file.

   .. image:: media/image25.png

#. Click the button :guilabel:`Import parameters from file` to import the
   parameters into the device.

   .. image:: media/image26.png

#. The software now writes the parameters into your device and stores them
   permanently into internal non-volatile memory.

   .. image:: media/image27.png

At the end of the parameter import, the software should report 
**"Parameter Import successful"**.

.. tip:: 
   If you get an error importing the parameters, you     
   should repeat the parameter import – sometimes this fixes   
   the problem.  

Device Parameter Export
~~~~~~~~~~~~~~~~~~~~~~~

.. rst-class:: steps

#. In the Parameter Export/Import dialog first click the :guilabel:`…`  button 
   on the right to select a parameter filename.

   .. image:: media/image25.png

#. In the Parameter File dialog navigate to the target folder, enter the
   name of the parameter file :guinum:`❶` and then click the :guilabel:`Open` button :guinum:`❷`.

   .. image:: media/image28.png

#. Click the button :guilabel:`Export parameters from file` to import the
   parameters into the device.

   .. image:: media/image29.png

#. The software now reads the parameters from the device and writes them
   into a :file:`*.dcf` file (Device Description File).

   .. image:: media/image30.png

At the end of the parameter export, the software should report 
**"Parameter Export successful"**.


Edit Device Parameters
----------------------

You can use der service tool to edit device parameters.

.. admonition:: Caution
   :class: error
  
   Before you edit any parameters, you should export  
   your current device parameters to restore them later in     
   case something goes wrong.  

.. admonition:: Caution
   :class: error
  
   Do only change parameters on request of the CETONI 
   service staff. If you change parameters without consulting  
   CETONI service staff, you may lose warranty in case of a    
   device error.   

.. rst-class:: steps

#. To open the parameter editor, click with the right mouse button on the
   node you would like to edit. Then select the menu item :guilabel:`Tools` from the
   context menu and in the Tools menu select :menuselection:`Object Dictionary`.

   .. image:: media/image31.png

#. The software now shows the object dictionary for the selected node. In
   the object dictionary view select :guilabel:`All Objects` from the *Active Object
   Filter* in the top right corner to show all object dictionary entries
   (see figure below).

   .. image:: media/image32.png

#. To edit a parameter, simply double click the parameter row:

   .. image:: media/image33.png

#. Now you can enter the new value :guinum:`❶` in the Edit Value Window and click 
   :guilabel:`OK` :guinum:`❷`.

   .. image:: media/image34.png

All edited parameters will get lost if the device is turned off or in
case of a reset. To save the changed parameters persistent into the
device non-volatile memory, click with right mouse button on the node
item in the left :guilabel:`Communication` panel and select :guilabel:`Save All Parameter` 
from the context menu.

.. image:: media/image35.png


Firmware Update
---------------

.. admonition:: Important
   :class: note

   To update the firmware, you need to be connected to your device – that
   means you have successfully completed the steps in section `Searching for devices (nodes)`_.


.. tip:: 
   To protect other devices from accidental updates, you 
   should only connect the device to your base module, that    
   you would like to update.   

.. rst-class:: steps

#. To open the Firmware Download Wizard, click with the right mouse button
   on the node you would like to update. Then select the menu item :menuselection:`Wizards`
   from the context menu and in the Wizards menu select 
   :menuselection:`Firmware Download Wizard`.

   .. image:: media/image36.png

#. In the window that appears, confirm the warning by clicking the :guilabel:`Confirm`
   button and then click the :guilabel:`Next >` button to continue.

   .. image:: media/image37.png

#. In the next step of the update wizard, you will see on the left :guinum:`❶` the
   firmware version, which is currently installed in the device. If the
   version matches the one you want to install, you can now exit the
   Fimware update.

   .. image:: media/image38.png

#. If the correct version is not installed in the device, click on the :guilabel:`…`
   button :guinum:`❷` to display the file dialog for selecting the
   firmware file. Select the firmware file according to the information
   provided by the CETONI support staff.

   .. tip:: 
      Normally the firmware files are located in 
      :code:`C:\Program Files (x86)\maxon motor ag\EPOS Positioning Controller\EPOS2\03 Configuration`   

#. Now you will see the version of the firmware update file on the right
   side. Click the :guilabel:`Next` button to start the firmware update.

   .. image:: media/image39.png

#. In the next wizard page, click the :guilabel:`…` button to select a
   writable folder for temporary storage of the exported device parameters.
   You can choose the Desktop folder here or any other writable folder.
   Then click the :guilabel:`Export` button to export the device configuration file
   (:file:`*.dcf`).

   .. image:: media/image40.png

#. After the parameter export, click the :guilabel:`Next` button to proceed. On the
   next Wizard page click the :guilabel:`Start` button to start the firmware download.

   .. image:: media/image41.png

#. Now wait, until the progress bar reaches 100% and proceed by clicking
   the :guilabel:`Next` button.

   .. image:: media/image42.png

#. On the next page of the Firmware wizard, you can reimport the previously
   exported device parameters. The input field should already contain the
   right parameter file. Click the :guilabel:`Import Parameter` button to start the
   parameter import.

   .. image:: media/image43.png

#. After the parameter import, you can click the :guilabel:`Next` button to finish the
   firmware download wizard.


Fixing Double-Module Node ID Conflict
-------------------------------------

If you have one Double Module connected to one Base Module, a device
scan with the EPOS Studio Software should show you two different node
identifiers – one for each pump channel of the double module. If only
one node has been detected, then there is likely a node conflict - i.e.
the two channels have the same node ID.

To fix the node conflict, do the following steps: 

.. rst-class:: steps

#. Connect only the Double Module to your base module – remove any other modules. 

#. Then set the service switch into **OFF** position (see picture above). 

#. Now scan for devices in EPOS Studio.

   |schalter_geraet| |schalter_geraet_zeichnung_02| 

   The scan in EPOS studio should detect one Node:

   .. image:: media/image46.png

   .. admonition:: Important
      :class: note

      If the software does not detect any node, then there is a hardware
      defect and you should contact the CETONI support for further
      instructions.

#. If the software has detected one node, then you can stop the scanning
   process and then click with the right mouse button on the node row in
   the table of scanned devices and select the menu item :menuselection:`Change Node-ID`
   from the context menu.

   .. image:: media/image47.png

#. Set the node ID to 114. Then rescan to verify that the software finds
   the node 114. The node 114 is now your left channel. Now set the service
   switch back into the **ON** position. Scan for devices in EPOS Studio. The
   software should find two nodes - the node 114 and a second node.

   .. image:: media/image48.png

#. Change the Node ID of the channel with the Node ID 144 to node ID
   113 and then set the node ID from Node 114 to 112 and rescan to verify
   that the two nodes are detected. The software should detect the two
   nodes 112 and 113.

   .. image:: media/image49.png

#. Now you can reconfigure your device in QmixElements software.

   .. admonition:: Important
      :class: note

      If you use a Starter Module instead of a BASE-Module then you might need
      to change the Node ID of the Starter Module to ID 115 before you connect
      the Double Module to avoid node ID conflicts with the Starter Module.




.. |schalter_geraet| image:: media/image44.png
   :width: 3.09375in
   :height: 2.44922in
.. |schalter_geraet_zeichnung_02| image:: media/image45.png
   :width: 3.03863in
   :height: 2.23958in
