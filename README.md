https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
sudo -i
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/sda -i flatcar/ignition.json
eject
reboot
~~~
https://github.com/docker/compose/releases/
~~~
sudo hostnamectl set-hostname
sudo curl -sL https://github.com/docker/compose/releases/download/$(curl -sL https://api.github.com/repos/docker/compose/releases | jq -r '.[0].name')/docker-compose-linux-x86_64 --create-dirs -o /opt/bin/docker-compose
sudo chmod +x /opt/bin/docker-compose
~~~

~~~
git clone https://github.com/ewalbridge/flatcar/
cd flatcar/n8n
docker-compose up -d
~~~
