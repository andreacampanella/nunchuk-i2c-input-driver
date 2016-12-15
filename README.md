## Synopsis

Based on Xerpi's code.

A Linux Kernel module driver for the Nintendo's Wii Nunchuk to act as an input device, in this case a mouse , for embedded devices like Raspberry Pi or CHIP (tested working on the Pocket Chip) 

## Motivation

Xerpi made and awesome job , I'm looking forward to expand the code with different modes (joystick for example) some improvements (interrupt driven?) and some debug info

## Installation

once copiled as a kernel module (tested on 4.4.13), load with
insmod nunchuk-i2c.ko 

and tell the kernel there is a new device with echo 

nunchuk-i2c 0x52 > /sys/bus/i2c/devices/i2c-2/new_device

(you will have to change your i2c channel according to your device)


