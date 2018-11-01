Expansion Board 3.0
===================

|image0|
--------

Datasheet
---------

The datasheet of the Expansion Board is available as a PDF File.

{% file src=“../../.gitbook/assets/expansion3-specsheet-1.pdf”
caption=“Expansion Board 3 Datasheet” %}

Pinout
------

The pinout of the Expansion Board is available as a PDF File

{% file src=“../../.gitbook/assets/expansion3-pinout.pdf”
caption=“Expansion Board 3 Pinout” %}

|image1|

{% hint style=“danger” %} Be gentle when plugging/unplugging from the
USB connector. Whilst the USB connector is soldered and is relatively
strong, if it breaks off it can be very difficult to fix. {% endhint %}

Battery Charger
---------------

The Expansion Board features a single cell Li-Ion/Li-Po charger. When
the board is being powered via the micro USB connector, the Expansion
Board will charge the battery (if connected). When the ``CHG`` jumper is
present the battery will be charged at ``450mA``. If this value is too
high for your application, removing the jumper lowers the charge current
to ``100mA``.

{% hint style=“info” %} To use the battery, pull ``P8/G15`` high
(connect to ``3v3``). If you want to use the SD card as well, use a 10k
pull-up. {% endhint %}

Differences between v2.0 and v3.0
---------------------------------

-  The FTDI chip as been replaced with a custom programmed PIC like on
   the

   Pysense/Pytrack/Pyscan boards. This allows our firmware update tool
   to

   automatically put the module into bootloader mode.

-  Added a “Safe boot” button to enter safe boot easier. This button
   connects

   ``P12`` to ``3.3v`` and if pressed and held while the reset button is
   pressed on

   a Pycom module, the module will enter safe boot.

Troubleshooting
---------------

-  If PIC stays in bootloader mode, the ```dfu-util``
   update <../../pytrackpysense/installation/firmware.md>`__ should be
   performed

.. |image0| image:: ../../.gitbook/assets/assets-lil0igdl11z7jos_jpx-lkn7scqkkkb6tqb3uyo-lkn82uldmpus0lnq1kx-expansion3.png
.. |image1| image:: ../../.gitbook/assets/expansion3-pinout-1.png

