# RPi2Bluez

## Steps to make ARM architecture based snap:
```
sudo apt-get update
sudo apt-get install ubuntu-dev-tools
sudo apt-get git
```
Run the following command twice for setting up the chroot env:
```
mk-sbuild --arch=armhf vivid
```
The first time it will install a bunch of packages and configure the environment. The second time, it will actually create the chroot.

chroot will get created in /var/lib/schroot/chroots/vivid-armhf
```
sudo sbuild-shell vivid-armhf
```

Use snappy tools to build the snap
```
snapcraft
```
