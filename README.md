https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
cd ~
git clone https://github.com/ewalbridge/flatcar/
flatcar-install -v -d /dev/sda -i flatcar/ignition.json
~~~
https://github.com/docker/compose/releases
~~~
sudo curl -SL https://github.com/docker/compose/releases/download/{latest}/docker-compose-linux-x86_64 --create-dirs -o /opt/docker/bin/docker-compose
sudo chmod +x /opt/docker/bin/docker-compose
cd flatcar/n8n
sudo /opt/docker/bin/docker-compose up -d
~~~
