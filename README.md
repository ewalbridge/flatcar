https://www.flatcar.org/docs/latest/installing/bare-metal/installing-to-disk/
~~~
git clone https://github.com/ewalbridge/flatcar/
cd flatcar/
flatcar-install -v -d /dev/sda -i flatcar/ignition.json
sudo curl -SL https://github.com/docker/compose/releases/download/{latest-version}/docker-compose-linux-x86_64 -o /opt/bin/docker-compose
sudo chmod x+ /opt/bin/docker-compose
cd n8n
/opt/bin/docker-compose up -d
~~~
