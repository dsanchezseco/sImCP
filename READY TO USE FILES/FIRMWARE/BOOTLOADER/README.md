# WARNING!!! You probably don't need these files

This files are to be used with and ISP flasher NOT with regular USB programming.

**If you do not know the terms MCU, ISP, BOOTLOADER or V-USB this is probably not for you.** You have been warned.

## You do not need these files unless the MCU is blank or you sourced the PCBs yourself


The files here are ready to flash a new MCU with both the **bootloader** and the **firmware**. There are two variants:

* QMK : regular [QMK](https://github.com/qmk/qmk_firmware) firmware to act as a keyboard. It uses *modifier/s+key* for each of the actions. Can have collisions with default game keybinds but it is recognized in every game/sim that uses a keyboard.
* Gamepad : custom firmware to act as a gamepad. It is recognized as an standalone device which uses buttons for each action. Do not have collisions with default keybinds but some games/sims may not recognized.

Both versions use (a modified version of ) [USBaspLoader](https://github.com/dsanchezseco/USBaspLoader) to be used with this specific PCB, do not use it with any other.

USBaspLoader provides V-USB (virtual USB) capabilities for not USB ready devices like the **atmega328p** being used here. This way the PCB can use a **low speed USB** controlled via software and **firmware flashing through USB**.

# Flashing - CAUTION!!!

TODO