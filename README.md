https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
winget install --id Fedora.CoreOS.butane
butane --pretty ignition.yaml --output ignition.json
~~~
~~~
sudo -i
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/xvda -i flatcar/ignition.json
eject
reboot
~~~
~~~
ssh core@flatcar
~~~
~~~
passwd
sudo hostnamectl set-hostname flatcar
sudo timedatectl set-timezone UTC
~~~
