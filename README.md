# ploopy_trackball_nano_scroll
**Disclaimer:** These instructions were composed by Llama 3.1, a machine learning model, and may contain inaccuracies. Additionally, flashing hardware carries inherent risks, and this guide does not guarantee any results. It is the user's sole responsibility to ensure the safety and functionality of their own hardware.

You can use the hex directly or compile the hex file from `scroll/keymap.c`. Please read the linked guides thoroughly. 

## Usage

When Num Lock is on, Ploopy Nano's drag scroll is enabled.

## Directly using the hex file

1. Read the guide on QMK Firmware Programming for Ploopy Nano Trackball: https://github.com/ploopyco/nano-trackball/wiki/Appendix-D%3A-QMK-Firmware-Programming
2. Use QMK Toolbox to install the hex file into your Ploopy Nano Scroll.

## Compiling the Hex File Yourself

If you want to compile the hex file yourself, see `scroll/keymap.c` and check the code if you want to modify. The code is based on:

* https://github.com/englmaxi/zmk-hid-trackball-interface
* https://github.com/notwil/qmk_keyboards

To compile:

1. Follow the QMK guide from the setup: https://docs.qmk.fm/newbs_getting_started
2. Read the compile part.
3. Put the `scroll` folder along with your `keymap.c` file into `qmk_firmware/keyboards/ploopyco/trackball_nano/keymaps/`. So there will be two folders there `default` and `scroll`.
4. Compile it with `qmk compile -kb ploopyco/trackball_nano -km scroll`
5. You will get a hex file in `qmk_firmware` folder iirc. 
6. Use QMK Toolbox, bootload the nano, and flash it using the hex file.
