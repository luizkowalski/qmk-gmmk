# Custom GMMK v2 p65 ISO firmware

### What is this?

This is my custom firmware for the GMMK v2 p65 ISO keyboard. It is based on the [GMMK v2 p65 ISO firmware with VIA](https://github.com/qmk/qmk_firmware/tree/master/keyboards/gmmk/gmmk2/p65/iso/keymaps/via)

### What is different?

* VIA support
* MacOS keymaps
* Link Time Optimization (LTO) enabled for a reduced firmware size
* <kbd>Fn</kbd> + <kbd>+</kbd>/<kbd>-</kbd> to change volume
* <kbd>Fn</kbd> + <kbd>1</kbd>/<kbd>2</kbd> to change brightness
* <kbd>Fn</kbd> + <kbd>,</kbd>/<kbd>.</kbd>/<kbd>/</kbd> to control playback
* <kbd>Fn</kbd> + <kbd>z</kbd>/<kbd>x</kbd>/<kbd>c</kbd>/<kbd>v</kbd> to control RGB animation
* <kbd>Fn</kbd> + <kbd>space</kbd> to reset the keyboard and put into bootloader mode
* More RGB animations (digital rain, typing heatmap, etc.)
* Caps Lock indicator
* Ability to circle through active windows with <kbd>Cmd</kbd> + <kbd>Esc</kbd> instead of <kbd>Cmd</kbd> + <kbd>`</kbd>

### How to use

```sh
git clone https://github.com/qmk/qmk_firmware
cd qmk_firmware
# Install dependencies with `make git-submodule`
curl -L https://github.com/luizkowalski/qmk-gmmk/archive/refs/heads/main.zip -o keyboards/gmmk/gmmk2/p65/iso/keymaps/kowalski.zip
tar -xvf keyboards/gmmk/gmmk2/p65/iso/keymaps/kowalski.zip -C keyboards/gmmk/gmmk2/p65/iso/keymaps/ --strip-components=1
qmk flash -kb gmmk/gmmk2/p65/iso -km kowalski
```
