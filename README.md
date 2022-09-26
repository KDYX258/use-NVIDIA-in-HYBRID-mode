# How to use NVIDIA dedicate GPU in HYBRID mode

***

## 1. Prerequisites
![](https://i.ibb.co/cYGmXWR/2022-09-26-16-33.png) 

Make sure you have selected `hybrid mode` in your `optimus settings` or in the `power manager`.

## 2. Create `Start.sh` file

`#!/bin/sh`

`__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia exec program-name`

![](https://i.ibb.co/JrD0h3K/2022-09-26-17-08.png)

1. Copy the command and put it in a "Start.sh" file.
2. Change `program-name` to the name of the program you want to use with your NVIDIA graphic card **!!!Without .desktop!!!**
3. Save `Start.sh` file and move it to the directory where the program's executable is.

## 3. Last step
![](https://i.ibb.co/p2xz86Z/2022-09-26-17-49.png)

1. Edit the `.desktop` file of the program you have chosen in the `/usr/share/applications` directory.
2. Change the "value" of `Exec` to the pathname of the `Start.sh` file.
3. Change the "value" of `Terminal` to `true`.
4. Done, now save everything and open the program from the start menu.
