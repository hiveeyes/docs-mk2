Pyscan
======

|image0|

Datasheet
---------

The datasheet of the Pyscan is available as a PDF File.

{% file src=“../../.gitbook/assets/pyscan-specsheet.pdf” caption=“Pyscan
Datasheet” %}

Pyscan Libraries
----------------

-  Pyscan libraries to use the RFID/NFC reader are located
   `here <https://github.com/pycom/pycom-libraries/tree/master/pyscan>`__
-  The accelerometer library is
   `here <https://github.com/pycom/pycom-libraries/blob/master/pytrack/lib/LIS2HH12.py>`__

{% hint style=“info” %} For the time being, we recommend to upload the
``MFRC630.mpy`` file via FTP due to current limitations of Pymakr that
will be fixed shortly. {% endhint %}

Libraries for the rest of the components will be added soon.

Pyscan components:
------------------

-  **Accelerometer**: ST LIS2HH12
-  **Ambient light sensor**: Lite-on LTR-329ALS-01
-  **RFID/NFC reader**: NXP MFRC63002HN, 151

Driver
------

The Windows 7 driver for Pyscan is located
`here <../../pytrackpysense/installation/firmware.md>`__.

For other Operating Systems there’s no driver required.

Pinout
------

The pinout of the Pyscan is available as a PDF File

{% file src=“../../.gitbook/assets/pyscan-pinout.pdf” caption=“Pyscan
Pinout” %}

|image1|

Battery Charger
---------------

The board features a single cell Li-Ion/Li-Po charger. When the board is
being powered via the micro USB connector, it will charge the battery
(if connected).

.. |image0| image:: ../../.gitbook/assets/assets-lil0igdl11z7jos_jpx-lkn7scqkkkb6tqb3uyo-lkn83hfia61dsuyojco-pyscan-new.png
.. |image1| image:: ../../.gitbook/assets/pyscan-pinout-1.png

