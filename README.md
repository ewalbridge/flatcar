https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
git clone https://github.com/ewalbridge/flatcar/
cd flatcar/
flatcar-install -v -d /dev/sda -i flatcar/ignition.json
sudo curl -SL https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
sudo chmod x+ /usr/local/bin/docker-compose
cd n8n
/opt/bin/docker-compose up -d
~~~
