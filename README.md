https://klepp.biz

### uploading image right now ... will finish at ~ 21:00 GMT+2 ###

## Devuan Chimaera with TDE https://trinitydesktop.org - the best desktop ever :)
Latest image for RPi. Tested on RPi3A+ / RPi3B+ / RPi 3B / RPI 3 / RPi 400

UID/PWD:

pi / pi
root / < no password >

After you wrote the image to SD/USB you will most likely find it easier to do these changes from the host:

- resize the root partition (2. partition of the image) to fill the remaining space of your card. Use gparted or what ever you prefer.
- networking is managed by network-manager-tde, so just use it
- copy your .ssh/id_rsa.pub to /home/pi/.ssh/authorized_keys

You'll need to set a root password when you first login:

$ sudo passwd root

TDE Language & keyboard are set to english, console keyboard is set to german. German languagepack is installed, you can change it with Trinity Control Center / Region / Language. Or you delete /home/pi/.trinity and start with the wizzard.

 ![Screenshot TDE14.1]

## Devuan Chimaera Minimal Image

Tested on RPi3A+ / RPi3B+ / RPi 3B / RPI 3 / RPi 400**

UID/PWD: 
```
pi / pi
root / <no password>
```

After you wrote the image to SD/USB you will most likely find it easier to do these changes from the host:
- resize the root partition (2. partition of the image) to fill the remaining space of your card. Use gparted or what ever you prefer.
- WLAN: you'll need to edit /etc/wpa_supplicant/wpa_supplicant.conf and enter your APs SSID and  PASSWORD.
- copy your .ssh/id_rsa.pub to /home/pi/.ssh/authorized_keys

You'll need to set a root password when you first login:
```
$ sudo passwd root
```



### Image: 
https://github.com/zwieblum/devuan-images/releases/download/2021.07.29/rpi3-2021-07-29.img.xz

---

## CoC desaster on LinuxCNC

Maybe some of you have read the ongoing debate about CoC & linuxcnc. Some people think they have to play policemen for the good of the others. Well, that's not my point of view. As there is no debate allowed over that topic and these policemen think their management bull * * * t is without alternative .. well, I think my LinuxCNC ISO remaster is not wanted any more, so I have deleted all remasters for amd64/raspberrypi/Orangepi. I wish these policemen good luck in destroying communities - they will prevail, without doubt.

***My LinuxCNC remasered ISOs will not be availabe any more - say thank you to the policemen .. and don't forget: OBEY***

---

#### Screenshots
![Screenshot TDE14.1](https://github.com/zwieblum/devuan-images/blob/master/Bildschirmfoto1.png)
