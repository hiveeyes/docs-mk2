Modem Firmware Update
=====================

{% hint style=“info” %} This article is only related to GPy, FiPy, and
G01 boards {% endhint %}

{% hint style=“danger” %} **Important**: When upgrading your modem for
the first time, even if you have updated it in the past with the old
firmware update method, you **MUST** use the “recovery” upgrade method
described below. Otherwise you will risk breaking your module {% endhint
%}

Please read the following instructions carefully as there are some
significant changes compared to the previous updater version.

Most importantly, the updater is now integrated in the latest stable
firmware release (we will also publish a new development and pybytes
firmware in the coming days), so you no longer need to upload any
scripts to your module. The built-in updater will take precedence over
any scripts uploaded.

Please start with the following steps:

1. Upgrade the Pycom Firmware Updater tool to latest version
2. Select Firmware Type ``stable`` in the communication window to
   upgrade to version ``v1.18.1.r1``

You can find the different versions of firmwares available here:
https://software.pycom.io/downloads/sequans2.html

We are using ``CATM1-38638.zip`` and ``NB1-37781.zip`` as examples in
this tutorial.

After unpacking the zip archive, you will find each firmware packages
contains two files, one being the firmware file (e.g.
``CATM1-38638.dup`` or ``NB1-37781.dup``) and the ``updater.elf`` file,
which is required when using the “recovery” firmware update method or if
a previous upgrade failed and the modem is in recovery mode.

Please note that the ``updater.elf`` file is only around 300K so you can
also store it inside the flash file system of the module. The firmware
dup files will NOT fit into the available ``/flash`` file system on the
module, so you either need to use an SD card or upload it directly from
your computer.

Via SD card
-----------

To transfer the firmware files onto the SD card you have two options:

1. Format your SD card as with the FAT file system and then copy the
   files onto the card using your computer
2. Make sure your SD card has an MBR and a single primary partition, the
   format it directly on the module, mount it and transfer the firmware
   files onto the SD card using FTP. Please ensure the transfer is
   successful and that each file on the module has the same size as the
   original file on your PC.

.. code:: python

   from machine import SD

   sd = SD()
   os.mkfs(sd)            # format SD card
   os.mount(sd, '/sd')    # mount it
   os.listdir('/sd')      # list its content

Once you copied/uploaded the firmware files on to the SD card you can
flash the LTE modem using the following command:

To flash the CAT-M1 firmware onto your device using the recovery method:

.. code:: python

   import sqnsupgrade
   sqnsupgrade.run('/sd/CATM1-38638.dup', '/sd/updater.elf')

To flash the NB-IoT firmware onto your device using the recovery method:

.. code:: python

   import sqnsupgrade
   sqnsupgrade.run('/sd/NB1-37781.dup', '/sd/updater.elf')

Please note you can directly flash the desired firmware onto your
module, it is not necessary to upgrade to the latest CAT-M1 firmware
before switching to NB-IoT.

If you have already mounted the SD card, please use the path you used
when mounting it. Otherwise, if an absolute path other than ``/flash``
is specified, the script will automatically mount the SD card using the
path specified.

Once update is finished successfully you will have a summary of new
updated versions. The full output from the upgrade will looks similar to
this:

.. code:: text

   <<< Welcome to the SQN3330 firmware updater >>>
   Attempting AT wakeup...
   Starting STP (DO NOT DISCONNECT POWER!!!)
   Session opened: version 1, max transfer 8192 bytes
   Sending 54854 bytes: [########################################] 100%
   Bootrom updated successfully, switching to upgrade mode
   Attempting AT auto-negotiation...
   Session opened: version 1, max transfer 2048 bytes
   Sending 306076 bytes: [########################################] 100%
   Attempting AT wakeup...
   Upgrader loaded successfully, modem is in upgrade mode
   Attempting AT wakeup...
   Starting STP ON_THE_FLY
   Session opened: version 1, max transfer 8192 bytes
   Sending 5996938 bytes: [########################################] 100%
   Code download done, returning to user mode
   Resetting (DO NOT DISCONNECT POWER!!!)................
   Upgrade completed!
   Here's the current firmware version:

   SYSTEM VERSION
   ==============
     FIRMWARE VERSION
       Bootloader0  : 5.1.1.0 [33080]
       Bootloader1  : 5.1.1.0 [38638]
       Bootloader2* : 5.1.1.0 [38638]
       NV Info      : 1.1,0,0
       Software     : 5.1.1.0 [38638] by robot-soft at 2018-08-20 09:51:46
       UE           : 5.0.0.0d
     COMPONENTS
       ZSP0         : 1.0.99-13604
       ZSP1         : 1.0.99-12341

{% hint style=“info” %} Please note that the firmware update may seem to
“stall” around 7-10% and again at 99%. This is not an indication of a
failure but the fact that the modem has to do some tasks during and the
updater will wait for these tasks to be completed. Unless the upgrade
process is hanging for more than 5 minutes, **do not interrupt the
process** as you will have to start again if you don’t finish it. It may
also take several minutes for the updater to load before responding to
the AT wakeup command. {% endhint %}

After you have updated your modem once using the recovery method, you
can now flash your modem again using just the ``CATM1-38638.dup`` or
``NB1-37781.dup`` file without specifying the ``updater.elf`` file.
However, should the upgrade fail, your modem may end up in recovery mode
and you will need the ``updater.elf`` file again. The updater will check
for this and prompt you if using the ``updater.elf`` file is necessary.

Example output using just the firmware file:

.. code:: text

   <<< Welcome to the SQN3330 firmware updater >>>
   Attempting AT wakeup...

   Starting STP ON_THE_FLY
   Session opened: version 1, max transfer 8192 bytes
   Sending 5996938 bytes: [########################################] 100%
   Code download done, returning to user mode
   Resetting (DO NOT DISCONNECT POWER!!!)............................................................................
   Upgrade completed!
   Here's the current firmware version:

   SYSTEM VERSION
   ==============
     FIRMWARE VERSION
       Bootloader0  : 5.1.1.0 [33080]
       Bootloader1* : 5.1.1.0 [38638]
       Bootloader2  : 5.1.1.0 [38638]
       NV Info      : 1.1,0,0
       Software     : 5.1.1.0 [38638] by robot-soft at 2018-08-20 09:51:46
       UE           : 5.0.0.0d
     COMPONENTS
       ZSP0         : 1.0.99-13604
       ZSP1         : 1.0.99-12341

Via UART Serial Interface
-------------------------

If you can’t use an SD card to hold the firmware images, you can use the
existing UART interface you have with the board to load these firmware
files from your Computer.

You will need the following software installed on your computer:

1. `Python 3 <https://www.python.org/downloads>`__, if it’s not directly
   available through your OS distributor
2. `PySerial <https://pythonhosted.org/pyserial/pyserial.html#installation>`__

You will also need to download the following Python scripts:
https://github.com/pycom/pycom-libraries/tree/master/lib/sqnsupgrade

**Important**: When upgrading your modem for the first time, even if you
have updated it in the past with the old firmware update method, you
**MUST** use the “recovery” upgrade method described below. Otherwise,
you will risk breaking your module.

You can upload the ``updater.elf`` file to the module’s flash file
system rather than uploading it via UART directly to the modem, which
will slightly increase the speed of the upgrade.

First, you need to prepare your modem for upgrade mode by using the
following commands.

**Commands to run on the Pycom module**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To use the recovery method:

.. code:: python

   import sqnsupgrade
   sqnsupgrade.uart(True)

To use the recovery method using the ``updater.elf`` file on the
module\ **:**

.. code:: python

    import sqnsupgrade
    sqnsupgrade.uart(True,'/flash/updater.elf')

To use the normal method:

.. code:: python

    import sqnsupgrade
    sqnsupgrade.uart()

After this command is executed a message will be displayed asking you to
close the port.

.. code:: text

   Going into MIRROR mode... please close this terminal to resume the upgrade via UART

**Commands to be run on your computer**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You must close the terminal/Atom or Visual Studio Code console to run
the following commands from your computer:

Go to the directory where you saved the ``sqnsupgrade`` scripts and run
the following commands in terminal:

When using the recovery method:

.. code:: python

   $ python3
   Python 3.6.5 (default, Apr 25 2018, 14:23:58)
   [GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.1)] on darwin
   Type "help", "copyright", "credits" or "license" for more information.
   >>>
   >>> import sqnsupgrade
   >>> sqnsupgrade.run('Serial_Port', '/path/to/CATM1-38638.dup', '/path/to/updater.elf')

When using the standard method (or if the ``updater.elf`` was loaded on
the module):

.. code:: python

    $ python3
    Python 3.6.5 (default, Apr 25 2018, 14:23:58)
    [GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.1)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    >>> import sqnsupgrade
    >>> sqnsupgrade.run('Serial_Port', '/path/to/CATM1-38638.dup')

Please note that the firmware update may seem to “stall” around 7-10%
and again at 99%. This is not an indication of a failure but the fact
that the modem has to do some tasks during and the updater will wait for
these tasks to be completed. Unless the upgrade process is hanging for
more than 5 minutes, **do not interrupt the process** as you will have
to start again if you don’t finish it. It may also take several minutes
for the updater to load before responding to the AT wakeup command.

Retrying process
----------------

In case of any failure or interruption to the process of LTE modem
upgrade you can repeat the same steps **after doing a hard reset to the
board (i.e disconnecting and reconnecting power), pressing the reset
button is not enough.**
