install QMK MSYS
fork and clone vial-qmk to some folder
start QMK MSYS
cd to vial-qmk folder
check if folder is correct with $ qmk env
flash firmware with code below
if some kind of chibios error occurs, try $ make git-submodule
then you can edit keymap in vial and load the layout file (silakka54.vil)

Make example for this keyboard (after setting up your vial build environment):

    qmk compile -kb silakka54 -km vial

Flashing example for this keyboard:

    qmk flash -kb silakka54 -km vial

## Bootloader

Enter the bootloader in 2 ways:


* **Double tap reset button
* **Physical boot button**: Hold BOOT button down and connect MCU to the PC
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available