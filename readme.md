# N2K Backpack

An ESP32 powered N2K wifi client, designed to broadcast a wifi NMEA source to displays or other devices.


## Installing

Requires micropython to install to an esp32:

* Install latest Python 3.x e.g

  ```
  echo "python 3.9.7" > .tool-versions
  asdf install
  ```

* Install esptool

  `pip install esptool`

* Download latest micropython kernel from: https://github.com/micropython/micropython/releases

* Use esptool.py to program the esp32.

  - On the first time use:

    `esptool.py --chip esp32 --port /dev/ttyUSB0 erase_flash`

  - After that program the firmware starting at address 0x1000:

    `esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 460800 write_flash -z 0x1000 esp32-20190125-v1.10.bin`

    Firmware is provided using either ESP-IDF v3.x or v4.x. If in doubt use v4.x.
