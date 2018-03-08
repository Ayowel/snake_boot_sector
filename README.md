# Snake game on MBR

Hi folks ! Here is one of my one weekend project that I made back in 2013. I find it funny and worth sharing.


# What is it ?

A custom MBR (Master Boot Record) booting a snake game. If left on an usb key it will boot instead of your system.

# ScreenToGif

![Alt Text](/snake.gif)

## Start from qemu
```sh
$ qemu-system-i386 snake.img
```

## Start from Virtualbox

Import snake.ova from virtualbox and start !!

## Start on your hardware using an USB key
```
sudo dd bs=512 if=snake.img of=/dev/YOUR_USB_KEY_DEVICE
```
*Replace YOUR_USB_KEY_DEVICE by your usb device (example: sdb or sdc).* Be careful if you choose the wrong device your computer might broke.

Booting on this USB device will not hurt your computer.

## Start from bochs
```sh
$ bochs 'boot:a' 'floppya: 1_44=snake.img, status=inserted'
```

---

By [@chaign\_c][] [#HexpressoTeam][hexpresso].


[hexpresso]:     https://hexpresso.github.io
[@chaign\_c]:    https://twitter.com/chaign_c
