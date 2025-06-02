https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
git clone https://github.com/ewalbridge/flatcar/
cd flatcar/
flatcar-install -v -d /dev/sda -i ignition.json
~~~

~~~
sudo curl -SL https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64 --create-dirs -o /opt/docker/bin/docker-compose
sudo mkdir -P /opt/docker/bin
sudo chmod x+ /opt/docker/bin/docker-compose
cd n8n
docker-compose up -d
~~~
