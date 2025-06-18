https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/

### Convert yaml file to json
~~~
winget install --id Fedora.CoreOS.butane
butane --pretty ignition.yaml --output ignition.json
~~~

### Boot flatcar iso and run the flatcar-install command as root
~~~
sudo -i
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/xvda -i flatcar/ignition.json
eject
reboot
~~~

### SSH to flatcar
~~~
ssh core@flatcar
~~~

### Change password, rename and set timezone
~~~
passwd #change default password
sudo hostnamectl set-hostname flatcar
sudo timedatectl set-timezone UTC
~~~

### Install XCP-ng vm tools
~~~
# mount guest-tools.iso
sudo -i
mount /dev/sr0 /media
/media/Linux/install.sh
sed -i 's|/usr/sbin/|/opt/oem/xs/|g' /etc/systemd/system/xe-linux-distribution.service
systemctl daemon-reload
systemctl enable /etc/systemd/system/xe-linux-distribution.service
~~~

### Install Portainer
~~~
docker run -d -p 8000:8000 -p 9000:9000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ee:lts
~~~
