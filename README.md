https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
sudo -i
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/xvda -i flatcar/ignition.json
eject
reboot

sudo hostnamectl set-hostname flatcar
passwd
~~~
