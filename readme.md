S60-X RGB PCB Custom Keymap for QMK
====

This is my custom keymap for my Sentraq 60% keyboard using the S60-X RGB PCB.

### Customize

The easiest way to customize this keymap is to load the included JSON into [kbfirmware.com](http://kbfirmware.com/) and go to town. From there you can download the compiled `.hex` file when you're done.

Alternately, you can edit `keymap.c` and build it in [QMK](https://github.com/qmk/qmk_firmware) yourself. For more info on that, see the [QMK docs](https://docs.qmk.fm/). It's not difficult to do, but for the average user, [kbfirmware.com](http://kbfirmware.com/) is going to be faster and will likely do everything you want it to.

### Flashing the PCB (Linux/Mac)

This is terrifying if you've never flashed firmware onto a chipset before, but it's really kind of hard to permenantly brick your PCB.

1. Download and install/compile [dfu-programmer](http://dfu-programmer.sourceforge.net/)
2. In the terminal, navigate to the directory where your `.hex` file is located.
3. Plug in your PCB via a mini-USB cable and press the programming button on the PCB.
4. Issue the following commands in the terminal

```
sudo dfu-programmer atmega32u4 erase
sudo dfu-programmer atmega32u4 flash s60xrgb.hex
sudo dfu-programmer atmega32u4 start
```

The keyboard should start working. If it doesn't, unplug it and plug it back in.
