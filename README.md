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
docker run -d -p 8000:8000 -p 9000:9000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:lts
~~~
