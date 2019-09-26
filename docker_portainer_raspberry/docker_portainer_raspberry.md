
# Installer Docker & Portainer sur Raspberry

## Introduction

## Pré-requis
- [Etcher](https://www.balena.io/etcher/) : logiciel qui nous permettra de flasher proprement la carte SD bootable pour le Raspberry
- [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) : l'OS de prédilection des Raspberry. La version à choisir dépend de votre besoin. Personnellement, j'utilise toujours mes Raspberry en tant que serveur, je prends donc systématiquement la version "Lite" quitte à installer manuellement des choses par la suite.
- Quelques bases en ligne de commandes
## Installation

### Flasher la carte SD
1. Insérez votre carte SD
2. Ouvrez Etcher
3. Choisissez l'image de Raspbian que vous avez téléchargé ainsi que le périphérique correspondant à votre carte SD puis cliquez sur "Flash".

![flash media](images/flash_media.png)

### Activer le SSH sur le Raspberry

### Installer Docker

### Installer Portainer

HDMI + Ethernet.
pi / raspberry (attention clavier QWERTY)
sudo -s
raspi-config
5 Interfacing Options
SSH enable
ssh pi@raspberrypi

https://docs.docker.com/install/linux/docker-ce/debian/#install-using-the-convenience-script

sudo systemctl status docker
https://www.portainer.io/installation/
curl -L https://downloads.portainer.io/portainer-agent-stack.yml -o portainer-agent-stack.yml
sudo docker swarm init
sudo docker stack deploy --compose-file=portainer-agent-stack.yml portainer
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc2MjE2OTAwNV19
-->