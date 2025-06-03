https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
sudo -i
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/sda -i flatcar/ignition.json
eject
reboot
~~~
