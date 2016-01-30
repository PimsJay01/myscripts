# myscripts
My personnal scripts

## scripts

- reset_bluetooth  Reset bluetooth
- unlock_apt_get   Unlock apt-get after update or installation problem

## Fix wifi issues

#RealTek RTL8821AE w/ Ubuntu 14.04 disconnect issues

http://ubuntuforums.org/showthread.php?t=2245164

This should work for realtek cards, enter one line at a time into terminal

```
wget -N -t 5 -T 10 https://www.kernel.org/pub/linux/kernel/projects/backports/stable/v3.18.1/backports-3.18.1-1.tar.xz
tar -xf backports-3.18.1-1.tar.xz
cd ~/backports-3.18.1-1
make defconfig-rtlwifi
make
sudo make install
```

After a kernel update you will need to

```
cd ~/backports-3.18.1-1
make clean
make defconfig-rtlwifi
make
sudo make install
```

