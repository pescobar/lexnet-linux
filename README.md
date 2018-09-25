# lexnet-linux

Contenedor [Singularity](https://www.sylabs.io/) con Firefox + Java configurado acceder a LexNET.

En pruebas...mas documentacion si consigo que funcione ;)


## Instalar Singularity

En Ubuntu

```bash
sudo apt-get update
sudo apt-get -y install build-essential squashfs-tools \
autoconf libtool bash-completion libarchive-dev
mkdir ~/src/ && cd ~/src/
wget https://github.com/singularityware/singularity/archive/2.6.0.tar.gz
tar xvf 2.6.0.tar.gz
cd singularity-2.6.0/
./autogen.sh
./configure --prefix=/usr/local
make
sudo make install
sudo ln -s /usr/local/etc/bash_completion.d/singularity /etc/profile.d/singularity.sh
```


