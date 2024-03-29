LoPy 4
======

Basic connection
----------------

{% tabs %} {% tab title=“Exp Board 2.0” %} \* Look for the reset button
on the module (located at a corner of the board, next to the LED). \*
Locate the USB connector on the expansion board. \* Insert the LoPy4
module on the the expansion board with the reset button pointing towards
the USB connector. It should firmly click into place and the pins should
now no longer be visible.

|image0| {% endtab %}

{% tab title=“Exp Board 3.0” %} \* Before connecting your module to an
Expansion Board 3.0, you should update the firmware on the Expansion
Board 3.0. Instructions on how to do this can be found
`here <../../pytrackpysense/installation/firmware.md>`__. \* Look for
the reset button on the module (located at a corner of the board, next
to the LED). \* Locate the USB connector on the expansion board. \*
Insert the LoPy4 module on the Expansion Board with the reset button
pointing towards the USB connector. It should firmly click into place
and the pins should now no longer be visible.

|image1| {% endtab %}

{% tab title=“Pytrack/Pysense/Pyscan” %} \* Before connecting your
module to a Pysense/Pytrack/Pyscan board, you should update the firmware
on the Pysense/Pytrack/Pyscan. Instructions on how to do this can be
found `here <../../pytrackpysense/installation/firmware.md>`__. \* Look
for the reset button on the LoPy4 module (located at a corner of the
board, next to the LED). \* Locate the USB connector on the
Pysense/Pytrack/Pyscan. \* Insert the module on the
Pysense/Pytrack/Pyscan with the reset button pointing towards the USB
connector. It should firmly click into place and the pins should now no
longer be visible.

|image2| |image3| {% endtab %}

{% tab title=“USB UART Adapter” %} \* Firstly you will need to connect
power to your LoPy4. You will need to supply ``3.5v``-``5.5v`` to the
``Vin`` pin.

{% hint style=“danger” %} Do **not** feed ``3.3v`` directly to the
``3.3v`` supply pin, this will damage the regulator. {% endhint %}

-  The connect the ``RX`` and ``TX`` of your USB UART to the ``TX`` and
   ``RX`` of the LoPy4 respectively.

{% hint style=“warning” %} Please ensure you have the signal level of
the UART adapter set to ``3.3v`` before connecting it. {% endhint %}

-  In order to put the LoPy4 into bootloader mode to update the device
   firmware you will need to connect ``P2`` to ``GND``. We recommend you
   connect a button between the two to make this simpler.

|image4| {% endtab %}

{% tab title=“WiFi” %} **Note:** This method of connection is not
recommended for first time users. It is possible to lock yourself out of
the device, requiring a USB connection.

-  In order to access the LoPy4 via WiFi you only need to provide
   ``3.5v`` - ``5.5v`` on the ``Vin`` pin of the LoPy4:

|image5|

-  By default, when the LoPy4 boots, it will create a WiFi access point
   with the following credentials:

   -  SSID: ``lopy4-wlan``
   -  password: ``www.pycom.io``

-  Once connected to this network you will be able to access the telnet
   and FTP servers running on the LoPy4. For both of these the login
   details are:

   -  username: ``micro``
   -  password: ``python`` {% endtab %} {% endtabs %}

Antennas
--------

Lora/Sigfox
~~~~~~~~~~~

{% hint style=“danger” %} If you intend on using the LoRa/Sigfox
connectivity of the LoPy4 you **must** connect a LoRa/Sigfox antenna to
your LoPy4 before trying to use LoRa/Sigfox otherwise you risk damaging
the device. {% endhint %}

-  Firstly you will need to connect the U.FL to SMA pig tail to the
   LoPy4 using one of the two the U.FL connectors on the same side of
   the LoPy4 as the LED. The one on the left hand side is for 433MHz
   (LoRa only), the one of the right hand side is for 868MHz/915MHz
   (LoRa & Sigfox). **Note:** This is different from the LoPy.

|image6|

-  If you are using a pycase, you will next need to put the SMA
   connector through the antenna hole, ensuring you align the flat edge
   correctly, and screw down the connector using the provided nut.
-  Finally you will need to screw on the antenna to the SMA connector.

|image7|

{% hint style=“danger” %} Since the LoRa chip only runs on one frequency
band at a time you only need to connect an antenna to the appropriate
U.FL connecor. You should be supplied with a the antenna that suits the
band you intend using. {% endhint %}

WiFi/Bluetooth (optional)
~~~~~~~~~~~~~~~~~~~~~~~~~

All Pycom modules, including the LoPy4, come with a on-board WiFi
antenna as well as a U.FL connector for an external antenna. The
external antenna is optional and only required if you need better
performance or are mounting the LoPy4 in such a way that the WiFi signal
is blocked. Switching between the antennas is done via software,
instructions for this can be found
`here. <../../firmwareapi/pycom/network/wlan.md>`__

|image8|

.. |image0| image:: ../../.gitbook/assets/expansion_board_2_lopy4.png
.. |image1| image:: ../../.gitbook/assets/expansion_board_3_lopy4.png
.. |image2| image:: ../../.gitbook/assets/assets-2f-lifiulge6_ztmmvcuea-2f-lkmxk1kqvbgjpw04i3u-2f-liqbk7blltxqntvqzh_-2fpysense_lopy4.png
.. |image3| image:: ../../.gitbook/assets/assets-2f-lifiulge6_ztmmvcuea-2f-lkmxk1kqvbgjpw04i3u-2f-liqbluw130dl1amaklt-2fpytrack_lopy4.png
.. |image4| image:: ../../.gitbook/assets/uart_lopy4.png
.. |image5| image:: ../../.gitbook/assets/bare_lopy4.png
.. |image6| image:: ../../.gitbook/assets/lora_sigfox_pigtail_lopy4.png
.. |image7| image:: ../../.gitbook/assets/lora_sigfox_pigtail_ant_lopy4.png
.. |image8| image:: ../../.gitbook/assets/wifi_pigtail_ant_lopy4.png

