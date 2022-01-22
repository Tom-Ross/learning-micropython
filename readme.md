# A short introduction to micropython

### Curriculum

* [Project 1](project1/readme.md)
  * switch outputs and react to inputs
* [Project 2](project2/readme.md)
  * switch outputs and react to inputs
* [Project 3](project3/readme.md)
  * switch outputs and react to inputs
* [Project 4](project4/readme.md)
  * switch outputs and react to inputs


### Getting started
* install esptools in your (project specific virtual) python environment

    `pip install esptools`

* if you are using PyCharm (IntellijIDEA) make sure micropython plugin is installed
  * **File -> Settings -> Plugin -> Marketplace** -> search for MicroPython
* download firmware for your board
    
    https://micropython.org/download/esp32/

    https://micropython.org/resources/firmware/esp32-20220117-v1.18.bin

* erase current image on microcontroller

    `esptool.py --chip esp32 --port /dev/ttyUSB0 erase_flash`

* flash micropython to microcontroller

    `esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 460800 write_flash -z 0x1000 esp32-20220117-v1.18.bin`


### Links
* Quick reference for the ESP32

  https://docs.micropython.org/en/latest/esp32/quickref.html


