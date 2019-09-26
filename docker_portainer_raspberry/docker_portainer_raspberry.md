
# Installer Docker & Portainer sur Raspberry

## Introduction

## Pré-requis
- [Etcher](https://www.balena.io/etcher/) : logiciel qui nous permettra de flasher proprement la carte SD bootable pour le Raspberry
- [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) : l'OS de prédilection des Raspberry. La version à choisir dépend de votre besoin. Personnellement, j'utilise toujours mes Raspberry en tant que serveur, je prends donc systématiquement la version "Lite" quitte à installer manuellement des choses par la suite.
- Quelques bases en ligne de commandes
## Installation

### Flasher la carte SD & bootez
1. Insérez votre carte SD
2. Ouvrez Etcher
3. Choisissez l'image de Raspbian que vous avez téléchargé ainsi que le périphérique correspondant à votre carte SD puis cliquez sur "Flash".

![flash media](images/flash_media.png)

4. Mettez la carte SD dans le Raspberry, brancher un câble Ethernet, l'alimentation ainsi qu'un clavier et un écran (via HDMI) qui nous seront utiles pour le premier boot.

### Activer le SSH sur le Raspberry
1. Une fois votre Raspberry démarré, loguez vous via l'utilisateur `pi` et le mot de passe par défaut : `raspberry`. **Attention, le clavier sera peut-être vu comme un QWERTY.**
2. Nous allons activer le serveur SSH du Raspberry, tapez : `sudo raspi-config` et faites la configuration suivante : Interfacing Options > SSH > Yes. Ci-après les écrans de configuration.

![interfacing options](images/interfacing_options.png)
![ssh options](ssh_options.png)
![ssh enable](images/enable_ssh.png)

C'est fini ! Vous pouvez débranche clavier et écran,
### Installer Docker

### Installer Portainer

ssh pi@raspberrypi

https://docs.docker.com/install/linux/docker-ce/debian/#install-using-the-convenience-script

sudo systemctl status docker
https://www.portainer.io/installation/
curl -L https://downloads.portainer.io/portainer-agent-stack.yml -o portainer-agent-stack.yml
sudo docker swarm init
sudo docker stack deploy --compose-file=portainer-agent-stack.yml portainer
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUzMzU5NDk4OCwxNzYyMTY5MDA1XX0=
-->