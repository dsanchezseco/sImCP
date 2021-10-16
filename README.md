# **sImCP**

or *simple ICP* for the friends

![simcp](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/sImCP.jpeg)

sImCP is **custom PCB** powered by an atmega328p to emulate the different aircraft up front controlers (UFC) and input control panels (ICP), mainly a mix of the F-18 and the F-16 panels but with support for others like the AV-8B or the A-10C, for flight simming in DCS an other simulators.

The origin of the project was to have something in the empty space of the MFD in my cockpit, and as such the holes align with the holes and mounting of the Thrustmaster MFDs

![mounted](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/mounted.jpg)

![mounted side](https://raw.githubusercontent.com/dsanchezseco/sImCP/main/images/mounted_side.jpg)


The features that define the **sImCP** are:

* Atmega328p
* USB-C
* 21 keys (MX or ALPS mechanical switches)
* 2 encoders with push
* 1 2-Way switch
* 1 4-Way with push and encoder (called dobber)
* [QMK](https://qmk.fm) support
* Thrustmaster Cougar MFD mountable

In fact it is a **fully programmable keyboard** and as such its keys behaviour can be changed by creating a new custom keymap with QMK and flashing it to the board

### It is a keyboard, so use the keyboard column on DCS to do the keybinds

### **Default keymap**

The default keymap has the following keycodes:

```

   ------------ ----------- ------------- ------------- ------------
   |  LCTL+A  | |  LCTL+O  | |  LCTL+U  | |  LCTL+I   | |  LCTL+D  |
   ------------ ------------ ------------ ------------- ------------
   ------------ ------------ ------------ ------------- ------------
   |  RCTL+1  | |  RCTL+2  | |  RCTL+3  | | ENCODER 1 | |  LCTL+H  |
   ------------ ------------ ------------ ------------- ------------
   ------------ ------------ ------------ ------------- ------------
   |  RCTL+4  | |  RCTL+5  | |  RCTL+6  | | ENCODER 2 | |  LCTL+T  | 
   ------------ ------------ ------------ ------------- ------------
   ------------ ------------ ------------ ------------- ------------
   |  RCTL+7  | |  RCTL+8  | |  RCTL+9  | |  2-WAY    | |  LCTL+N  |
   ------------ ------------ ------------ ------------- ------------
   ------------ ------------ ------------ ------------- ------------
   |  RCTL+]  | |  LCTL+0  | |  RCTL+[  | |  DOBBER   | |  LCTL+;  |
   ------------ ------------ ------------ ------------- ------------



#########################################
   ENCODER 1
#########################################
  RCTL+F   LCTL+Q    RCTL+C
   (         |         )
   v         v         v


#########################################
   ENCODER 2
#########################################
  RCTL+Y   LCTL+J    RCTL+G
   (         |         )
   v         v         v

#########################################
   2-WAY
#########################################
  LCTL+K
    ^
    |

    |
    v
  LCTL+X

#########################################
   DOBBER
#########################################
          LCTL+M                     
            ^                        
            |                       RCTL+B   RCTL+W    RCTL+Z 
LCTL+P <-       -> LCTL+R            (         |         )
            |                        v         v         v
            v
          LCTL+W
```

### **Gamepad**

Instead of being recognised as a keyboard the sImCP can be flashed with a custom made firmware to act as a gamepad and output a button instead a keycode on each of the keys. 

**This feature is currently WIP**

### **Flashing** 

To flash a new keymap refeer to the [FIRMWARE README.md](READY%20TO%20USE%20FILES/FIRMWARE/README.md) under the `READY TO USE FILES` folder. The default keymap file is provided as well in the same folder.

### READY TO USE inventory

* PCB_FABRICATION: what's needed to order more to JLCPCB already in the correct format
* PCB_3DMODEL: in case you want to print something :)
* FIRMWARE: the code to make it running ready to flash
* 3D_PRINTABLES: stuff ready to print like the **dobber cap (by Joghurt - thanks!)**