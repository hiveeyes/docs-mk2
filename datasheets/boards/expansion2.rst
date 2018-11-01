Expansion Board 2.0
===================

|image0|

Datasheet
---------

The datasheet of the Expansion Board is available as a PDF File.

{% file src=“../../.gitbook/assets/expansion2-specsheet.pdf”
caption=“Expansion Board 2 Datasheet” %}

Pinout
------

The pinout of the Expansion Board is available as a PDF File

{% file src=“../../.gitbook/assets/expansion2-pinout.pdf”
caption=“Expansion Board 2 Pinout” %}

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

.. |image0| image:: ../../.gitbook/assets/assets-lil0igdl11z7jos_jpx-lkn7scqkkkb6tqb3uyo-lkn86jsexys_ho7ct7c-expansion2.png
.. |image1| image:: ../../.gitbook/assets/expansion2-pinout-1.png

