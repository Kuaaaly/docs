# Installer Docker & Portainer sur Raspberry

## Introduction

Docker est devenu un must-have pour les développeurs et les administrateurs systèmes ces derniers temps. N'importe quel personne se revendiquant "DevOps" en fera presque systématiquement usage au quotidien. Je ne vais pas ici vous expliquer précisément ce qu'est Docker, ni comment il fonctionne car de nombreuses ressources sur internet sont disponibles et expliquent cela bien mieux que je ne pourrais le faire.

Je me sers de Docker au quotidien, au travail comme à la maison. C'est un outil génial pour déployer rapidement du code / des applications sans polluer allègrement votre système. Vous permettant ainsi de redémarrer "from scratch" indéfiniement sans jamais avoir à refaire une installation système complète.

Dans cette documentaiton, je vous explique pas à pas comment installer sur un Raspberry :

* [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) : un système d'exploitation pour le Raspberry \(dérivé de Debian\)
* [Docker](http://docker.com) : pour déployer nos conteneurs et les "orchestrer" \(via Docker Swarm\)
* [Portainer](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=2ahUKEwif1NDphcflAhVLCxoKHbgrD-gQFjAAegQIAxAB&url=https%3A%2F%2Fwww.portainer.io%2F&usg=AOvVaw1fQe4vdV5aFnpnWUeHvRT_) : pour contrôler tout cela directement via notre navigateur web sans \(jamais\) avoir à nous reconnecter en SSH à notre précieux Raspberry.

Une dernière petite note, personnelle cette fois-ci. À la maison, j'ai à la fois :

* Un vieux laptop x64 qui me fait office de seveur sur lequel je déploie mes applications stables & pérennes.
* Un Raspberry qui me fait office de bac à sable pour mes développements et mes tests.

Dans les 2 cas, ce sont Docker et Portainer qui me permettent de faire mes déploiements. Certains d'entre vous me dirons que les architectures CPU des deux "serveurs" ne sont pas les mêmes \(x64 vs. ARM\). Effectivement, parfois cela est bloquant car certains conteneurs ne fonctionnent pas sous ARM, ces cas restes assez rares et pour l'instant je n'ai pas eu de gros blocage.

## Pré-requis

* [Etcher](https://www.balena.io/etcher/) : logiciel qui nous permettra de flasher proprement la carte SD bootable pour le Raspberry
* [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) : l'OS de prédilection des Raspberry. La version à choisir dépend de votre besoin. Personnellement, j'utilise toujours mes Raspberry en tant que serveur, je prends donc systématiquement la version "Lite" quitte à installer manuellement des choses par la suite.
* Quelques bases en ligne de commandes

## **Installation**

### Flasher la carte SD & bootez

1. Insérez votre carte SD
2. Ouvrez Etcher
3. Choisissez l'image de Raspbian que vous avez téléchargé ainsi que le périphérique correspondant à votre carte SD puis cliquez sur "Flash".

![flash media](../../.gitbook/assets/flash_media.png)

1. Mettez la carte SD dans le Raspberry, branchez un câble Ethernet, l'alimentation ainsi qu'un clavier et un écran \(via HDMI\) qui nous seront utiles pour le premier boot.

### Activer le SSH sur le Raspberry

1. Une fois votre Raspberry démarré, loguez vous via l'utilisateur `pi` et le mot de passe par défaut : `raspberry`. **Attention, le clavier sera peut-être vu comme un QWERTY.**
2. Nous allons activer le serveur SSH du Raspberry, tapez : `sudo raspi-config` et faites la configuration suivante : **Interfacing Options &gt; SSH &gt; Yes**. Ci-après les écrans par lesquels vous devez passer.

![interfacing options](../../.gitbook/assets/interfacing_options.png) ![ssh options](../../.gitbook/assets/ssh_options.png) ![ssh enable](../../.gitbook/assets/enable_ssh.png)

C'est fini ! Vous pouvez débrancher clavier et écran, ils ne vous serviront plus.

### Installer Docker

Dans la plupart des cas, le Raspberry va "s'annoncer" correctement auprès de votre routeur \(via son service mDNS\) et prendra le hostname `raspberrypi` sur le réseau. Vous pourrez donc facilement vous y connecter.

Installons désormais Docker :

1. Depuis votre terminal préféré \(via un ordinateur présent sur le même réseau\) :  


   ```bash
   ssh pi@raspberrypi //(mot de passe : raspberry)
   ```

2. Nous allons suivre [les instructions de Docker](https://docs.docker.com/install/linux/docker-ce/debian/#install-using-the-convenience-script) et utiliser le script officiel pour installer Docker \(soyez patients, le script met un peu de temps à tout installer\)  


   ```bash
   curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh get-docker.sh
   ```

3. Une fois que vous avez récupéré la main, vous pouvez taper la commande suivante pour vérifier que Docker est bien "running" :  


   ```bash
   sudo systemctl status docker
   ```

![docker running](../../.gitbook/assets/docker_running.png)

### Installer Portainer

Dernière étape, nous allons vouloir installer [Portainer](http://portainer.io) pour gérer facilement et graphiquement nos conteneurs Docker, nos services et nos stacks.

1. Initialiser Docker Swarm \(l'orchestrateur natif de Docker\), c'est lui qui vous permettra de déployer des stacks \(ensembles de conteneurs\) et par extensions des services, conteneurs, volumes, etc.  


   ```bash
   sudo docker swarm init
   ```

2. Télécharger le fichier de stack de Portainer :  


   ```bash
   curl -L https://downloads.portainer.io/portainer-agent-stack.yml -o portainer-agent-stack.yml
   ```

3. Déployer la stack :  


   ```bash
   sudo docker stack deploy --compose-file=portainer-agent-stack.yml portainer
   ```

4. Portainer est désormais accessible via votre navigateur à l'adresse suivante : [http://raspberrypi:9000](http://raspberrypi:9000).

Configurez le compte administrateur. **Attention, de mémoire il faut créer le compte administrateur dans les 5 premières minutes, sinon Portainer s'arrête par sécurité** :

![portainer login](../../.gitbook/assets/portainer_login.png)

Vous voilà rendu sur l'interface de Portainer !

![portainer ui](../../.gitbook/assets/portainer_ui.png)

Nous nous retrouverons dans un autre billet pour apprendre à l'utiliser. 

