FiPy
====

Basic connection
----------------

{% tabs %} {% tab title=“Exp Board 2.0” %} \* When using the expansion
board with a FiPy, you will need to remove the CTS and RTS jumpers as
these interfere with communication with the cellular modem. \* Look for
the reset button on the module (located at a corner of the board, next
to the LED). \* Locate the USB connector on the expansion board. \*
Insert the FiPy module on the the expansion board with the reset button
pointing towards the USB connector. It should firmly click into place
and the pins should now no longer be visible.

|image0| {% endtab %}

{% tab title=“Exp Board 3.0” %} \* Before connecting your module to an
Expansion Board 3.0, you should update the firmware on the Expansion
Board 3.0. Instructions on how to do this can be found
`here <../../pytrackpysense/installation/firmware.md>`__. \* When using
the expansion board with a FiPy, you will need to remove the CTS and RTS
jumpers as these interfere with communication with the cellular modem.
\* Look for the reset button on the module (located at a corner of the
board, next to the LED). \* Locate the USB connector on the expansion
board. \* Insert the FiPy module on the Expansion Board with the reset
button pointing towards the USB connector. It should firmly click into
place and the pins should now no longer be visible.

|image1| {% endtab %}

{% tab title=“Pytrack/Pysense/Pyscan” %} \* Before connecting your
module to a Pysense/Pytrack/Pyscan board, you should update the firmware
on the Pysense/Pytrack/Pyscan. Instructions on how to do this can be
found `here <../../pytrackpysense/installation/firmware.md>`__. \* Look
for the reset button on the FiPy module (located at a corner of the
board, next to the LED). \* Locate the USB connector on the
Pysense/Pytrack/Pyscan. \* Insert the module on the
Pysense/Pytrack/Pyscan with the reset button pointing towards the USB
connector. It should firmly click into place and the pins should now no
longer be visible. |image2|\ |image3| {% endtab %}

{% tab title=“USB UART Adapter” %} \* Firstly you will need to connect
power to your FiPy. You will need to supply ``3.5v``-``5.5v`` to the
``Vin`` pin.

{% hint style=“danger” %} Do **not** feed ``3.3v`` directly to the
``3.3v`` supply pin, this will damage the regulator. {% endhint %}

-  The connect the ``RX`` and ``TX`` of your USB UART to the ``TX`` and
   ``RX`` of the FiPy respectively.

{% hint style=“warning” %} Please ensure you have the signal level of
the UART adapter set to ``3.3v`` before connecting it. {% endhint %}

-  In order to put the FiPy into bootloader mode to update the device
   firmware you will need to connect ``P2`` to ``GND``. We recommend you
   connect a button between the two to make this simpler.

|image4| {% endtab %}

{% tab title=“WiFi” %} **Note:** This method of connection is not
recommended for first time users. It is possible to lock yourself out of
the device, requiring a USB connection.

-  In order to access the FiPy via WiFi you only need to provide
   ``3.5v`` - ``5.5v`` on the ``Vin`` pin of the FiPy:

|image5|

-  By default, when the FiPy boots, it will create a WiFi access point
   with the following credentials:

   -  SSID: ``fipy-wlan``
   -  password: ``www.pycom.io``

-  Once connected to this network you will be able to access the telnet
   and FTP servers running on the FiPy. For both of these the login
   details are:

   -  username: ``micro``
   -  password: ``python`` {% endtab %} {% endtabs %}

Antennas
--------

Lora/Sigfox
~~~~~~~~~~~

{% hint style=“danger” %} If you intend on using the LoRa/Sigfox
connectivity of the FiPy you **must** connect a LoRa/Sigfox antenna to
your FiPy before trying to use LoRa/Sigfox otherwise you risk damaging
the device. {% endhint %}

{% hint style=“info” %} The FiPy only supports LoRa on the 868MHz or
915MHz bands. It does not support 433MHz. For this you will require a
LoPy4. {% endhint %}

-  Firstly you will need to connect the U.FL to SMA pig tail to the FiPy
   using the U.FL connector on the same side of the FiPy as the LED.

|image6|

-  If you are using a pycase, you will next need to put the SMA
   connector through the antenna hole, ensuring you align the flat edge
   correctly, and screw down the connector using the provided nut.
-  Finally you will need to screw on the antenna to the SMA connector.

|image7|

LTE Cat-M1/NB-IoT
~~~~~~~~~~~~~~~~~

{% hint style=“danger” %} If you intend on using the LTE CAT-M1 or
NB-IoT connectivity of the FiPy you **must** connect a LTE CAT-M1/NB-IoT
antenna to your FiPy before trying to use LTE Cat-M1 or NB-IoT otherwise
you risk damaging the device. {% endhint %}

-  You will need to connect the antenna to the FiPy using the U.FL
   connector on the under side of the FiPy.

|image8|

WiFi/Bluetooth (optional)
~~~~~~~~~~~~~~~~~~~~~~~~~

All Pycom modules, including the FiPy, come with a on-board WiFi antenna
as well as a U.FL connector for an external antenna. The external
antenna is optional and only required if you need better performance or
are mounting the FiPy in such a way that the WiFi signal is blocked.
Switching between the antennas is done via software, instructions for
this can be found `here. <../../firmwareapi/pycom/network/wlan.md>`__

|image9|

SIM card 
~~~~~~~~~

If you intend on using the LTE CAT-M1 or NB-IoT connectivity of the FiPy
you will need to insert a SIM card into your FiPy. It should be noted
that the FiPy does not support regular LTE connectivity and you may
require a special SIM. It is best to contact your local cellular
providers for more information on acquiring a LTE CAT-M1/NB-IoT enabled
nano SIM.

|image10|

.. |image0| image:: ../../.gitbook/assets/expansion_board_2_fipy.png
.. |image1| image:: ../../.gitbook/assets/expansion_board_3_fipy.png
.. |image2| image:: https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LIfiUlGe6_zTmmvcuEa%2F-LKMXk1KQvBgjpw04I3u%2F-LIqVauBuoNMgcByrNql%2FPysense_FiPy.png?generation=1534772069160637&alt=media
.. |image3| image:: https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LIfiUlGe6_zTmmvcuEa%2F-LKMXk1KQvBgjpw04I3u%2F-LIqVdDdxkK38AlRxtkc%2FPytrack_FiPy.png?generation=1534772071490748&alt=media
.. |image4| image:: ../../.gitbook/assets/uart_fipy.png
.. |image5| image:: ../../.gitbook/assets/bare_fipy.png
.. |image6| image:: ../../.gitbook/assets/lora_sigfox_pigtail_fipy.png
.. |image7| image:: ../../.gitbook/assets/lora_sigfox_pigtail_ant_fipy.png
.. |image8| image:: ../../.gitbook/assets/lte_ant_fipy.png
.. |image9| image:: ../../.gitbook/assets/wifi_pigtail_ant_fipy.png
.. |image10| image:: ../../.gitbook/assets/sim_fipy.png

