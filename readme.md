# A short introduction to micropython

### Curriculum

* [Project 1](project1/readme.md)
    * control outputs and react to inputs
* [Project 2](project2/readme.md)
    * button memory game
* [Project 3](project3/readme.md)
    * digital thermometer
* [Project 4](project4/readme.md)
    * network based multiuser thermometer
* [Project 5](project4/readme.md)
    * multiplayer button memory game

### Getting started

* download USB-driver for CP210x

  https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers

* install esptools in your (project specific virtual) python environment

  `pip install esptool`

* if you are using PyCharm (IntellijIDEA) make sure micropython plugin is installed
    * **File -> Settings -> Plugin -> Marketplace** -> search for MicroPython
* download firmware for your board

  https://micropython.org/download/esp32/

  https://micropython.org/resources/firmware/esp32-20220117-v1.18.bin

* erase current image on microcontroller

  `esptool.py --chip esp32 --port /dev/ttyUSB0 erase_flash`

* flash micropython to microcontroller

  `esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 460800 write_flash -z 0x1000 esp32-20220117-v1.18.bin`

### Note

* In some cases it might be necessary to store secrets like Wi-Fi credentials.

  **These must not be committed into public repositories!**

  For these values use `secrets.py` which is listed in `.gitignore`.

    * secrets.py

      `SUPER_SECRET_WLAN_PASSWORD = '1234'`

    * main.py

      `from secrets import SUPER_SECRET_WLAN_PASSWORD`

### Links

* Quick reference for the ESP32

  https://docs.micropython.org/en/latest/esp32/quickref.html


