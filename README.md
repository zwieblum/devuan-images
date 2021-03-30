https://klepp.biz

# devuan-images
This dumpyard is dedicated to my systemd-free remasterings based on devuan + extras. All images default to german localisation and keymap. Oh, and I had the strong feeling the ISOs should get a name. So I call them "Maschinist".

## amd64
### Exegnulinux remasterd with LinuxCNC - amd64

* Devuan 3.1 (no systemd, yeah!) based Exegnulinux + TDE 14.1 https://trinitydesktop.org + LinuxCNC 2.8.1 + HTML Docs, NCAM, PREEMPT Kernel, smictrl, ... and a whole toolkit to get going
* F-Engrave, dmap2gcode, g-Code_Ripper, pycam 0.7, dxf2gcode, pcb2gcode & pcb2gcodeGUI, KiCad, Gimp, Inkscape,  Slic3r, Printrun, OpenScad ... and some more :)
* Arduino IDE

PREEMPT RT:
* ISO: https://github.com/zwieblum/devuan-images/releases/download/2021.04/maschinist_rt_2021-04.iso
* SHA256: https://github.com/zwieblum/devuan-images/releases/download/2021.04/maschinist_rt_2021-04.iso.sha256

RTAI Kernel:
* ISO: https://github.com/zwieblum/devuan-images/releases/download/2021.04/maschinist_rtai_2021-04.iso
* SHA256: https://github.com/zwieblum/devuan-images/releases/download/2021.04/maschinist_rtai_2021-04.iso.sha256

Release 2021.04 and up:  **root** / **toor** and **user** / **user**. 

## arm
### RaspberryPi 3+

* Devuan + TDE 14.1
* Image: https://github.com/zwieblum/devuan-images/releases/download/2021.04.rpi/rpi3+_chimaera_tde.img.xz

After dd the image to your SD-card or USB-stick, boot the Pi, use "raspi-config" to maximize root partition.

### OrangePi PC Plus

* Devuan on top of Armbian, without X11: https://github.com/zwieblum/devuan-images/releases/download/20200926/devuan-beowulf-orangepipcplus-2GB-20200926.img.xz
* Devuan on top of Armbian, with TDE: https://github.com/zwieblum/devuan-images/releases/download/20200926-2/devuan-beowulf-orangepipcplus-tde-2.3GB-20200926.img.xz

Sorry, no image with LinuxCNC for now. The last available RT kernel does not activate USB, so no keyboard or mouse, which contradicts the purpose of having X11 on the unit.

### OrangePi Zero (LTS)

* Devuan on top of Armbian, without X11: https://github.com/zwieblum/devuan-images/releases/download/20200926-1/devuan-beowulf-orangepizero-2G-2020-09-26.img.xz
* Devuan on top of Armbian, with LinuxCNC 2.7.15: https://github.com/zwieblum/devuan-images/releases/download/20200926-3/devuan-beowulf-orangepizero-linuxcnc-2.7.15-3G-20200926.img.xz

You can run LinuxCNC over SSH or forward the display without SSH to your computer - or you install VNC and use that for the GUI. 

### All arm Images

Write an image to the sd-card:
`xz devuan-beowulf-orangepipcplus-tde-2.3GB-20200926.img > /dev/sdXXX`

You will want to expand the image to take all the remaining space. Use `gparted`, but do not move the partition to the - otherwise you will overwrite the bootloader. 

User accounts are **root** / **root** and **user** / **user**. 
Release 2021.04 and up:  **root** / **toor** and **user** / **user**. 

#### Post-installation tasks:

Remove my ssh key (in case I forgot): `rm /root/.ssh/autorized_keys /home/user/.ssh/autorized_keys`
Change keyboard: `dpkg-reconfigure keyboard-configuration`
Change locales: `dpkg-reconfigure locales`
TDE full installation: `aptitude install tde-trinity`
And you might want to change the passwords ...

## Screenshots
![Screenshot TDE14.1](https://github.com/zwieblum/devuan-images/blob/master/Bildschirmfoto1.png)
