.. include:: include/colors.rst

.. role:: sg-yellow-bg
.. role:: sg-green-bg  
.. role:: sg-blue-bg
.. role:: sg-pink-bg


BASE 120 / BASE 600 Firmware Update
===================================

Preparation
-----------

Connect your BASE module to your PC. Start the software **Vci3floadGui** or
**Vci4floadGui** via Windows Explorer. You will find the software in
:code:`C:\Program Files\IXXAT\3.5 or C:\Program Files\HMS\IXXAT VCI 4.0` after
the installation of the QmixElements or Nemesys User Interface software
(see figure below).

.. image:: media/image98.png

The software will show you the detected USB-to-CAN interface. If the
software does not detect any USB-to-CAN interface then please try to
connect your BASE module to another USB interface of your PC.

You only need to do an update, if you have a **V2** device, that means, if
you have an **USB-to-CAN V2 embedded** or an **USB-to-CAN V2 compact**. If you
do not have a V2 device, then you are finished now.

Update procedure
----------------

An USB-to-CAN V2 device should appear in the Device field :guinum:`❶` of the
Flashloader window.

.. image:: media/image99.png

Click the :guilabel:`>>`` button :guinum:`❷` to select the firmware (e.g.
:file:`USB-to-CAN_V2_FW_0_1_6_3_R380.hex`). You will find the latest firmware
here:

https://CETONI.de/software-downloads/

.. admonition:: Attention
   :class: caution

   Do not interrupt the process while the flash     
   procedure is running! 

Now click the :guilabel:`Flash` button to start the update process :guinum:`❹`. Wait for the
process to complete and then click :guilabel:`Verify`. If the verification succeeds
with an OK message (see Figure below) the update process is complete and
your device has been updated successfully.

.. image:: media/image100.png