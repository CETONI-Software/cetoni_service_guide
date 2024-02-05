.. include:: include/colors.rst

.. role:: sg-yellow-bg
.. role:: sg-green-bg  
.. role:: sg-blue-bg
.. role:: sg-pink-bg


Nemesys UserInterface
=====================

Edit Device Configuration
-------------------------

Starting the Configuration Wizard
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. rst-class:: steps

#. Start the Nemesys UserInterface and scan for devices with your pump
   attached. Select the pump you would like to configure by clicking on the
   label on top of the pump. The label of the selected pump will be
   highlighted green.

   .. image:: media/image90.png

#. Enter the service mode by clicking the menu item :menuselection:`Setup --> Enter Service Mode`.

   .. image:: media/image91.png

#. Enter the service password epos241 into the password field that appears.

   .. image:: media/image92.png

#. The title bar now indicates that you are working in service mode.

   .. image:: media/image93.png

#. Select the menu item :menuselection:`Setup Configure Axis` from the main menu

   .. image:: media/image94.png

#. The **Nemesys Configuration Wizard** appears.

   .. image:: media/image95.png

#. Click the :guilabel:`Next` button until you see the desired configuration page.

Setting the Gear Factor
~~~~~~~~~~~~~~~~~~~~~~~

.. rst-class:: steps

Start the configuration wizard like written in the section above and
navigate to the wizard page **Step 2 – Configuring Pump**. On this page, you
can see the gear factor on the left:

.. image:: media/image96.png

Ensure that the gear factor matches the physical device configuration
and modify it accordingly. Finally click :guilabel:`Save configuration into device`
to store the changes in non-volatile device memory. Then close the
configuration wizard and execute a device scan to apply your changes.

.. image:: media/image97.png