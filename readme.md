S60-X RGB PCB Custom Keymap for QMK
====

This is my custom keymap for my Sentraq 60% keyboard using the S60-X RGB PCB.

####Customize

The easiest way to customize this keymap is to load the included JSON into [kbfirmware.com](http://kbfirmware.com/) and go to town. From there you can download the compiled `.hez` file when  you're done.

Alternately, you can edit `keymap.c` and build it in [QMK](https://github.com/qmk/qmk_firmware) yourself. For more info on that, see the [QMK docs](https://docs.qmk.fm/). - It's not difficult to do, but for the average user, [kbfirmware.com](http://kbfirmware.com/) is going to be faster and will likely do everything you want it to.

####Flashing the PCB (Linux/Mac)

1. Download and install/compile [dfu-programmer](http://dfu-programmer.sourceforge.net/)
2. Issue the following commands in the command prompt after connecting the device and pressing the programming button on the PCB (S1).

    sudo dfu-programmer atmega32u4 erase
    sudo dfu-programmer atmega32u4 flash [name of hex file]
    sudo dfu-programmer atmega32u4 start

The keyboard should start working. If it doesn't, unplug it and plug it back in.