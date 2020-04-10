### enabling Wifi through SD card
```
sudo nano /etc/wpa_supplicant/wpa_supplicant.conf 
```

copy and paste the following into wpa_supplicant.conf 
```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=US

network={
    ssid="HomeOneSSID"
    psk="passwordOne"
    priority=1
}
```

### enabling SSH through SD card

add a new empty file and name is "ssh" and place it into boot drive 

#### if the above step does not enable ssh, then perform the following

ssh is installed but not started by default on runlevel 2, the default for raspbian.
Rename ```/etc/rc2.d/ssh/K??ssh``` to ```/etc/rc2.d/ssh/S02ssh```

#### Pi-hole setup instructions

link : https://blog.cryptoaustralia.org.au/instructions-for-setting-up-pi-hole/
