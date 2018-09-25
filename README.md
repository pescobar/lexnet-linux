# lexnet-linux

Contenedor [Singularity](https://www.sylabs.io/) con Firefox + Java configurado para acceder a LexNET.

[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/1727)

## Instalar Singularity

En debian stretch o ubuntu 16.10 o mas recientes:

 `sudo apt-get install singularity-container`

Para compilar desde las fuentes en ubuntu/debian:

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

Para instalar en otras distros: [documentacion oficial](https://www.sylabs.io/guides/2.6/user-guide/installation.html)

## Descargar y ejecutar el contenedor

```bash
singularity pull --name lexnet.simg shub://pescobar/lexnet-linux
./lexnet.simg
```
