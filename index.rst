.. Pycom Documentation documentation master file, created by
   sphinx-quickstart on Thu Nov  1 15:13:27 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root toctree directive.

Welcome to Pycom Documentation's documentation!
===============================================

.. toctree::
   :maxdepth: 3

   :caption: Contents:
   Introduction <README.md>
   Pycom Products <products.md>

   :caption: Getting Started
   Introduction <gettingstarted/introduction.md>
   Hardware Setup <gettingstarted/connection/README.md>
      LoPy <gettingstarted/connection/lopy.md>
      LoPy 4 <gettingstarted/connection/lopy4.md>
      SiPy <gettingstarted/connection/sipy.md>
      GPy <gettingstarted/connection/gpy.md>
      FiPy <gettingstarted/connection/fipy.md>
      WiPy <gettingstarted/connection/wipy.md>
   Software <gettingstarted/installation/README.md>
      Drivers <gettingstarted/installation/drivers.md>
      Updating Firmware <gettingstarted/installation/firmwaretool.md>
      Pymakr <gettingstarted/installation/pymakr.md>
   Programming the modules <gettingstarted/programming/README.md>
      Introduction to
         MicroPython <gettingstarted/programming/micropython.md>
      MicroPython Examples <gettingstarted/programming/examples.md>
      Your first Pymakr project <gettingstarted/programming/first-project.md>
      REPL <gettingstarted/programming/repl/README.md>
         Serial USB (UART) <gettingstarted/programming/repl/serial.md>
         Telnet REPL <gettingstarted/programming/repl/telnet.md>
      FTP <gettingstarted/programming/ftp.md>
      Safe boot <gettingstarted/programming/safeboot.md>
   Device Registration <gettingstarted/registration/README.md>
      Sigfox <gettingstarted/registration/sigfox.md>
      Cellular <gettingstarted/registration/cellular.md>
      LoRaWAN <gettingstarted/registration/lora/README.md>
         The Things Network <gettingstarted/registration/lora/ttn.md>
         Senet <gettingstarted/registration/lora/senet.md>
   Troubleshooting Guide <gettingstarted/troubleshooting-guide.md>__

   :caption: Pymakr Plugin
   Installation <pymakr/installation/README.md>__
      Atom <pymakr/installation/atom.md>
      Visual Studio Code <pymakr/installation/vscode.md>__
   Tools/Features <pymakr/toolsfeatures.md>__
   Settings <pymakr/settings.md>__

   :caption: Pytrack, Pysense, Pyscan
   Introduction <pytrackpysense/introduction.md>__
   Installing Software <pytrackpysense/installation/README.md>__
      Updating Firmware <pytrackpysense/installation/firmware.md>__
      Installing Drivers Windows 7 <pytrackpysense/installation/drivers.md>__
      Installing Libraries <pytrackpysense/installation/libraries.md>__
   API Reference <pytrackpysense/apireference/README.md>__
      Pytrack <pytrackpysense/apireference/pytrack.md>__
      Pysense <pytrackpysense/apireference/pysense.md>__
      Pyscan <pytrackpysense/apireference/pyscan.md>__
      Sleep <pytrackpysense/apireference/sleep.md>__

   :caption: Tutorials & Examples
   Introduction <tutorials/introduction.md>__
   All Pycom Device Examples <tutorials/all/README.md>__
      REPL <tutorials/all/repl.md>__
      WLAN <tutorials/all/wlan.md>__
      Bluetooth <tutorials/all/ble.md>__
      HTTPS <tutorials/all/https.md>__
      MQTT <tutorials/all/mqtt.md>__
      AWS <tutorials/all/aws.md>__
      ADC <tutorials/all/adc.md>__
      I2C <tutorials/all/i2c.md>__
      Onewire Driver <tutorials/all/owd.md>__
      Threading <tutorials/all/threading.md>__
      RGB LED <tutorials/all/rgbled.md>__
      Timers <tutorials/all/timers.md>__
      PIR Sensor <tutorials/all/pir.md>__
      Modbus <tutorials/all/modbus.md>__
      OTA update <tutorials/all/ota.md>__
      RMT <tutorials/all/rmt.md>__
   LoRa Examples <tutorials/lora/README.md>__
      LoRa-MAC (Raw LoRa) <tutorials/lora/lora-mac.md>__
      LoRaWAN with OTAA <tutorials/lora/lorawan-otaa.md>__
      LoRaWAN with ABP <tutorials/lora/lorawan-abp.md>__
      LoRa-MAC
         Nano-Gateway <tutorials/lora/lora-mac-nano-gateway.md>__
      LoPy to LoPy <tutorials/lora/module-module.md>__
      LoRaWAN Nano-Gateway <tutorials/lora/lorawan-nano-gateway.md>__
      RN2483 to LoPy <tutorials/lora/rn2483-to-lopy.md>__
   Sigfox Examples <tutorials/sigfox.md>__
   LTE Examples <tutorials/lte/README.md>__
      CAT-M1 <tutorials/lte/cat-m1.md>__
      NB-IoT <tutorials/lte/nb-iot.md>__
      Module IMEI <tutorials/lte/imei.md>__
      Modem Firmware Update <tutorials/lte/firmware.md>__
   Pytrack Examples <tutorials/pytrack.md>__
   Pysense Examples <tutorials/pysense.md>__
   Pyscan Examples <tutorials/pyscan.md>__

   :caption: Firmware & API Reference
   Introduction <firmwareapi/introduction.md>__
   Pycom Modules <firmwareapi/pycom/README.md>__
      machine <firmwareapi/pycom/machine/README.md>__
         ADC <firmwareapi/pycom/machine/adc.md>__
         DAC <firmwareapi/pycom/machine/dac.md>__
         I2C <firmwareapi/pycom/machine/i2c.md>__
         Pin <firmwareapi/pycom/machine/pin.md>__
         PWM <firmwareapi/pycom/machine/pwm.md>__
         RTC <firmwareapi/pycom/machine/rtc.md>__
         SPI <firmwareapi/pycom/machine/spi.md>__
         UART <firmwareapi/pycom/machine/uart.md>__
         WDT <firmwareapi/pycom/machine/wdt.md>__
         Timer <firmwareapi/pycom/machine/timer.md>__
         SD <firmwareapi/pycom/machine/sd.md>__
         CAN <firmwareapi/pycom/machine/can.md>__
         RMT <firmwareapi/pycom/machine/rmt.md>__
      network <firmwareapi/pycom/network/README.md>__
         WLAN <firmwareapi/pycom/network/wlan.md>__
         Server <firmwareapi/pycom/network/server.md>__
         Bluetooth <firmwareapi/pycom/network/bluetooth/README.md>
            GATT <firmwareapi/pycom/network/bluetooth/gatt.md>__
            GATTCConnection <firmwareapi/pycom/network/bluetooth/gattcconnection.md>__
            GATTCService <firmwareapi/pycom/network/bluetooth/gattccservice.md>__
            GATTCCharacteristic <firmwareapi/pycom/network/bluetooth/gattccharacteristic.md>__
            GATTSService <firmwareapi/pycom/network/bluetooth/gattsservice.md>__
            GATTSCharacteristic <firmwareapi/pycom/network/bluetooth/gattscharacteristic.md>__
         LoRa <firmwareapi/pycom/network/lora.md>__
         Sigfox <firmwareapi/pycom/network/sigfox.md>__
         LTE <firmwareapi/pycom/network/lte.md>__
      AES <firmwareapi/pycom/aes.md>__
      pycom <firmwareapi/pycom/pycom.md>__
   MicroPython Modules <firmwareapi/micropython/README.md>__
      micropython <firmwareapi/micropython/micropython.md>__
      uctypes <firmwareapi/micropython/uctypes.md>__
      sys <firmwareapi/micropython/sys.md>__
      uos <firmwareapi/micropython/uos.md>__
      array <firmwareapi/micropython/array.md>__
      cmath <firmwareapi/micropython/cmath.md>__
      math <firmwareapi/micropython/math.md>__
      gc <firmwareapi/micropython/gc.md>__
      ubinascii <firmwareapi/micropython/ubinascii.md>__
      ujson <firmwareapi/micropython/ujson.md>__
      ure <firmwareapi/micropython/ure.md>__
      usocket <firmwareapi/micropython/usocket.md>__
      select <firmwareapi/micropython/select.md>__
      utime <firmwareapi/micropython/utime.md>__
      uhashlib <firmwareapi/micropython/uhashlib.md>__
      ussl <firmwareapi/micropython/ussl.md>__
      ucrypto <firmwareapi/micropython/ucrypto.md>__
      ustruct <firmwareapi/micropython/ustruct.md>__
      \_thread <firmwareapi/micropython/_thread.md>__
      Builtin <firmwareapi/micropython/builtin.md>__
   Notes <firmwareapi/notes.md>__

   :caption: Product Info, Datasheets
   Introduction <datasheets/introduction.md>__
   Development Modules <datasheets/development/README.md>__
      WiPy 2.0 <datasheets/development/wipy2.md>__
      WiPy 3.0 <datasheets/development/wipy3.md>__
      LoPy <datasheets/development/lopy.md>__
      LoPy 4 <datasheets/development/lopy4.md>__
      SiPy <datasheets/development/sipy.md>__
      GPy <datasheets/development/gpy.md>__
      FiPy <datasheets/development/fipy.md>__
   OEM Modules <datasheets/oem/README.md>__
      W01 <datasheets/oem/w01.md>__
      L01 <datasheets/oem/l01.md>__
      L04 <datasheets/oem/l04.md>__
      G01 <datasheets/oem/g01.md>__
      L01 OEM Baseboard Reference <datasheets/oem/l01_reference.md>__
      Universal OEM Baseboard Reference <datasheets/oem/universal_reference.md>__
   Expansion Boards and Shields <datasheets/boards/README.md>__
      Expansion Board 3.0 <datasheets/boards/expansion3.md>__
      Pytrack <datasheets/boards/pytrack.md>__
      Pysense <datasheets/boards/pysense.md>__
      Pyscan <datasheets/boards/pyscan.md>__
      Expansion Board 2.0 <datasheets/boards/expansion2.md>__
      Deep Sleep Shield <datasheets/boards/deepsleep/README.md>__
         Deep Sleep API <datasheets/boards/deepsleep/api.md>__
   Notes <datasheets/notes.md>__

   :caption: Pybytes
   Introduction <pybytes/introduction.md>__
   Getting Started with Pybytes <pybytes/getstarted.md>__
   Add a device to Pybytes <pybytes/connect/README.md>__
      Connect to Pybytes: Quick Add <pybytes/connect/quick.md>__
      Connect to Pybytes: Flash Pybytes library manually <pybytes/connect/flash.md>__
      Add Sigfox device <pybytes/connect/sigfox/README.md>__
         DevKit contract <pybytes/connect/sigfox/devkit.md>__
         Custom contract <pybytes/connect/sigfox/custom.md>__
   Visualise data from your device <pybytes/dashboard.md>__

   :caption: Documentation Notes
   Introduction <docnotes/introduction.md>__
   Syntax <docnotes/syntax.md>__
   REPL vs Scripts <docnotes/replscript.md>__
   Mesh Networks <docnotes/mesh-networks.md>__

   :caption: Advanced Topics
   Firmware Downgrade <advance/downgrade.md>
   CLI Updater <advance/cli.md>
   SecureBoot and Encryption <advance/encryption.md>

   :caption: Documents
   Certificates <documents/certificates.md>
   License <documents/license.md>

   :caption: Have a question?
   Ask on the Forum <https://forum.pycom.io>

Indices and tables
==================

* :ref:genindex
* :ref:modindex
* :ref:search
