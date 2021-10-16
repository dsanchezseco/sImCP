These files are the firmware for the sImCP keyboard. There are two variants

* QMK : regular [QMK](https://github.com/qmk/qmk_firmware) firmware to act as a keyboard. It uses *modifier/s+key* for each of the actions. Can have collisions with default game keybinds but it is recognized in every game/sim that uses a keyboard.
* Gamepad : custom firmware to act as a gamepad. It is recognized as an standalone device which uses buttons for each action. Do not have collisions with default keybinds but some games/sims may not recognized.

# Flashing - CAUTION!!!

This is a delicate operation. Please follow all the steps and in case of doubt do not procced, **ASK FOR HELP**
## Preparation

1. Grab a piece of wire, tweezers or something conductive to be able to short the `boot` jumper 
2. Download and install [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) (can be used with any of the versions)
3. Download the desired `FIRMWARE` from this same folder

## Flashing

1. unplug the board
2. open QMK toolbox
3. click on open and select the downloaded .hex file

![select the hex file](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-1.png)
￼
4. under MCU select atmega328p

![select the MCU](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-2.png)

5. bridge the BOOT pins with a piece of wire or tweezers

![bridge boot](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-2.1.jpg)

1. Connect the board. The green power light should be off and on the toolbox you should see the yellow line (you can keep the bridge in, if the light goes on, try again, the light has to stay off)
![MCU recognized](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-3.png)

￼

### VERIFY YOU HAVE atmega328p SELECTED!

7. Click on Flash to start the process DO NOT UNPLUG THE BOARD OR CLOSE THE TOOLBOX!

![flash](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-4.png)
￼

When the process is finished you should see
￼

8. Reconnect the board  or briefly bridge the RESET pins and you are done

![done](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/flashing-5.png)
