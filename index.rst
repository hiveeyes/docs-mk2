.. Pycom Documentation documentation master file, created by
   sphinx-quickstart on Thu Nov  1 15:13:27 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root toctree directive.

Welcome to Pycom Documentation's documentation!
===============================================

.. toctree::
  :maxdepth: 1
  :caption: Contents

  Introduction <README>
  Pycom Products <products>

.. toctree::
  :maxdepth: 3
  :caption: Getting Started

  Introduction <gettingstarted/introduction>
  Hardware Setup <gettingstarted/connection/README>
    LoPy <gettingstarted/connection/lopy>
    LoPy 4 <gettingstarted/connection/lopy4>
    SiPy <gettingstarted/connection/sipy>
    GPy <gettingstarted/connection/gpy>
    FiPy <gettingstarted/connection/fipy>
    WiPy <gettingstarted/connection/wipy>
  Software <gettingstarted/installation/README>
    Drivers <gettingstarted/installation/drivers>
    Updating Firmware <gettingstarted/installation/firmwaretool>
    Pymakr <gettingstarted/installation/pymakr>
  Programming the modules <gettingstarted/programming/README>
    Introduction to MicroPython <gettingstarted/programming/micropython>
    MicroPython Examples <gettingstarted/programming/examples>
    Your first Pymakr project <gettingstarted/programming/first-project>
    REPL <gettingstarted/programming/repl/README>
      Serial USB (UART) <gettingstarted/programming/repl/serial>
      Telnet REPL <gettingstarted/programming/repl/telnet>
    FTP <gettingstarted/programming/ftp>
    Safe boot <gettingstarted/programming/safeboot>
  Device Registration <gettingstarted/registration/README>
    Sigfox <gettingstarted/registration/sigfox>
    Cellular <gettingstarted/registration/cellular>
    LoRaWAN <gettingstarted/registration/lora/README>
      The Things Network <gettingstarted/registration/lora/ttn>
      Senet <gettingstarted/registration/lora/senet>
  Troubleshooting Guide <gettingstarted/troubleshooting-guide>

.. toctree::
  :caption: Pymakr Plugin
  :maxdepth: 3

   Installation <pymakr/installation/README>
      Atom <pymakr/installation/atom>
      Visual Studio Code <pymakr/installation/vscode>
   Tools/Features <pymakr/toolsfeatures>
   Settings <pymakr/settings>

.. toctree::
  :caption: Pytrack, Pysense, Pyscan
  :maxdepth: 3

  Introduction <pytrackpysense/introduction>
  Installing Software <pytrackpysense/installation/index>
  API Reference <pytrackpysense/apireference/index>

.. toctree::
  :caption: Tutorials & Examples
  :maxdepth: 3

   Introduction <tutorials/introduction>
   All Pycom Device Examples <tutorials/all/README>
      REPL <tutorials/all/repl>
      WLAN <tutorials/all/wlan>
      Bluetooth <tutorials/all/ble>
      HTTPS <tutorials/all/https>
      MQTT <tutorials/all/mqtt>
      AWS <tutorials/all/aws>
      ADC <tutorials/all/adc>
      I2C <tutorials/all/i2c>
      Onewire Driver <tutorials/all/owd>
      Threading <tutorials/all/threading>
      RGB LED <tutorials/all/rgbled>
      Timers <tutorials/all/timers>
      PIR Sensor <tutorials/all/pir>
      Modbus <tutorials/all/modbus>
      OTA update <tutorials/all/ota>
      RMT <tutorials/all/rmt>
   LoRa Examples <tutorials/lora/README>
      LoRa-MAC (Raw LoRa) <tutorials/lora/lora-mac>
      LoRaWAN with OTAA <tutorials/lora/lorawan-otaa>
      LoRaWAN with ABP <tutorials/lora/lorawan-abp>
      LoRa-MAC
         Nano-Gateway <tutorials/lora/lora-mac-nano-gateway>
      LoPy to LoPy <tutorials/lora/module-module>
      LoRaWAN Nano-Gateway <tutorials/lora/lorawan-nano-gateway>
      RN2483 to LoPy <tutorials/lora/rn2483-to-lopy>
   Sigfox Examples <tutorials/sigfox>
   LTE Examples <tutorials/lte/README>
      CAT-M1 <tutorials/lte/cat-m1>
      NB-IoT <tutorials/lte/nb-iot>
      Module IMEI <tutorials/lte/imei>
      Modem Firmware Update <tutorials/lte/firmware>
   Pytrack Examples <tutorials/pytrack>
   Pysense Examples <tutorials/pysense>
   Pyscan Examples <tutorials/pyscan>

.. toctree::
  :caption: Firmware & API Reference
  :maxdepth: 3

   Introduction <firmwareapi/introduction>
   Pycom Modules <firmwareapi/pycom/README>
      machine <firmwareapi/pycom/machine/README>
         ADC <firmwareapi/pycom/machine/adc>
         DAC <firmwareapi/pycom/machine/dac>
         I2C <firmwareapi/pycom/machine/i2c>
         Pin <firmwareapi/pycom/machine/pin>
         PWM <firmwareapi/pycom/machine/pwm>
         RTC <firmwareapi/pycom/machine/rtc>
         SPI <firmwareapi/pycom/machine/spi>
         UART <firmwareapi/pycom/machine/uart>
         WDT <firmwareapi/pycom/machine/wdt>
         Timer <firmwareapi/pycom/machine/timer>
         SD <firmwareapi/pycom/machine/sd>
         CAN <firmwareapi/pycom/machine/can>
         RMT <firmwareapi/pycom/machine/rmt>
      network <firmwareapi/pycom/network/README>
         WLAN <firmwareapi/pycom/network/wlan>
         Server <firmwareapi/pycom/network/server>
         Bluetooth <firmwareapi/pycom/network/bluetooth/README>
            GATT <firmwareapi/pycom/network/bluetooth/gatt>
            GATTCConnection <firmwareapi/pycom/network/bluetooth/gattcconnection>
            GATTCService <firmwareapi/pycom/network/bluetooth/gattccservice>
            GATTCCharacteristic <firmwareapi/pycom/network/bluetooth/gattccharacteristic>
            GATTSService <firmwareapi/pycom/network/bluetooth/gattsservice>
            GATTSCharacteristic <firmwareapi/pycom/network/bluetooth/gattscharacteristic>
         LoRa <firmwareapi/pycom/network/lora>
         Sigfox <firmwareapi/pycom/network/sigfox>
         LTE <firmwareapi/pycom/network/lte>
      AES <firmwareapi/pycom/aes>
      pycom <firmwareapi/pycom/pycom>
   MicroPython Modules <firmwareapi/micropython/README>
      micropython <firmwareapi/micropython/micropython>
      uctypes <firmwareapi/micropython/uctypes>
      sys <firmwareapi/micropython/sys>
      uos <firmwareapi/micropython/uos>
      array <firmwareapi/micropython/array>
      cmath <firmwareapi/micropython/cmath>
      math <firmwareapi/micropython/math>
      gc <firmwareapi/micropython/gc>
      ubinascii <firmwareapi/micropython/ubinascii>
      ujson <firmwareapi/micropython/ujson>
      ure <firmwareapi/micropython/ure>
      usocket <firmwareapi/micropython/usocket>
      select <firmwareapi/micropython/select>
      utime <firmwareapi/micropython/utime>
      uhashlib <firmwareapi/micropython/uhashlib>
      ussl <firmwareapi/micropython/ussl>
      ucrypto <firmwareapi/micropython/ucrypto>
      ustruct <firmwareapi/micropython/ustruct>
      \_thread <firmwareapi/micropython/_thread>
      Builtin <firmwareapi/micropython/builtin>
   Notes <firmwareapi/notes>

.. toctree::
  :caption: Product Info, Datasheets
  :maxdepth: 3

   Introduction <datasheets/introduction>
   Development Modules <datasheets/development/README>
      WiPy 2.0 <datasheets/development/wipy2>
      WiPy 3.0 <datasheets/development/wipy3>
      LoPy <datasheets/development/lopy>
      LoPy 4 <datasheets/development/lopy4>
      SiPy <datasheets/development/sipy>
      GPy <datasheets/development/gpy>
      FiPy <datasheets/development/fipy>
   OEM Modules <datasheets/oem/README>
      W01 <datasheets/oem/w01>
      L01 <datasheets/oem/l01>
      L04 <datasheets/oem/l04>
      G01 <datasheets/oem/g01>
      L01 OEM Baseboard Reference <datasheets/oem/l01_reference>
      Universal OEM Baseboard Reference <datasheets/oem/universal_reference>
   Expansion Boards and Shields <datasheets/boards/README>
      Expansion Board 3.0 <datasheets/boards/expansion3>
      Pytrack <datasheets/boards/pytrack>
      Pysense <datasheets/boards/pysense>
      Pyscan <datasheets/boards/pyscan>
      Expansion Board 2.0 <datasheets/boards/expansion2>
      Deep Sleep Shield <datasheets/boards/deepsleep/README>
         Deep Sleep API <datasheets/boards/deepsleep/api>
   Notes <datasheets/notes>

.. toctree::
  :caption: Pybytes
  :maxdepth: 3

   Introduction <pybytes/introduction>
   Getting Started with Pybytes <pybytes/getstarted>
   Add a device to Pybytes <pybytes/connect/README>
      Connect to Pybytes: Quick Add <pybytes/connect/quick>
      Connect to Pybytes: Flash Pybytes library manually <pybytes/connect/flash>
      Add Sigfox device <pybytes/connect/sigfox/README>
         DevKit contract <pybytes/connect/sigfox/devkit>
         Custom contract <pybytes/connect/sigfox/custom>
   Visualise data from your device <pybytes/dashboard>

.. toctree::
  :caption: Documentation Notes
  :maxdepth: 1

  Introduction <docnotes/introduction>
  Syntax <docnotes/syntax>
  REPL vs Scripts <docnotes/replscript>
  Mesh Networks <docnotes/mesh-networks>

.. toctree::
  :caption: Advanced Topics
  :maxdepth: 1

  Firmware Downgrade <advance/downgrade>
  CLI Updater <advance/cli>
  SecureBoot and Encryption <advance/encryption>

.. toctree::
  :caption: Documents
  :maxdepth: 1

  Certificates <documents/certificates>
  License <documents/license>

.. toctree::
  :caption: Have a question?
  :maxdepth: 1

  Ask on the Forum <https://forum.pycom.io>
