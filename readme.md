# Lily58

1. install qmk 
```sh
paru qmk
``` 
2. run setup 
```sh
qmk setup

cd /home/$USER/qmk_firmware/keyboards/lily58
```

3. copy keymap to via (as we doing via setup)
```sh
cp keymaps/default keymap/via 
```

4. add via support in `keymaps/via/rules.mk`
```sh 
VIA_ENABLE = yes            # Enable VIA support
```

5. happy coding

6. compile and move firmware (via keymap)
```sh
qmk_firmware on  master [?] via 🐍 v3.13.3 
❯ qmk compile -kb lily58 -km via -e CONVERT_TO=promicro_rp2040 

qmk_firmware on  master [?] via 🐍 v3.13.3 took 12s 
❯ cp lily58_rev1_via_promicro_rp2040.uf2 /run/media/ketan/RPI-RP2/
```

7. (optional) to update image
- I edited font and render as logo in `glcdfont_lily.c` 
- used [QMK Logo Editor](https://joric.github.io/qle/) 


Lily58 is 6×4+5keys column-staggered split keyboard.

![Lily58_01](https://user-images.githubusercontent.com/6285554/50394214-72479880-079f-11e9-9d91-33fdbf1d7715.jpg)
![2018-12-24 17 39 58](https://user-images.githubusercontent.com/6285554/50394779-05360200-07a3-11e9-82b5-066fd8907ecf.png)
Keyboard Maintainer: [Naoki Katahira](https://github.com/kata0510/) [Twitter:@F_YUUCHI](https://twitter.com/F_YUUCHI)  
Hardware Supported: Lily58 PCB, ProMicro  
Hardware Availability: [PCB & Case Data](https://github.com/kata0510/Lily58)

Make example for this keyboard (after setting up your build environment):

    make lily58:default

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).


