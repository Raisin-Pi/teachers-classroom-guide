# Connexion à distance à un Raspberry Pi à partir d'un ordinateur en réseau

## Etape 1: Configurez et installez VNC server sur Raspberry Pi

Installez le logiciel VNC Server sur Pi et le logiciel de VNC Viewer sur l'ordinateur hôte (qui montrera le bureau Pi).

1. Sur votre Raspberry Pi installez le package TightVNC:

  ```
  sudo apt-get install tightvncserver
  ```
1. Ensuite, exécutez TightVNC Server qui vous invite à entrer un mot de passe et une option de visualisation du mot de passe:

  ```
  tightvncserver
  ```

1. Démarrez un serveur VNC à partir du terminal. Cet exemple démarre une session sur l'affichage VNC zéro (```:0```) avec une résolution Full HD:

  ```
  vncserver :0 -geometry 1024x768 -depth 24
  ```

## Étape 2: Installez un client VNC sur un ordinateur

1. Maintenant, sur votre ordinateur, installez et exécutez le client VNC:

  - Sur une machine Linux, installez le paquet `xtightvncviewer`:

    `sudo apt-get install xtightvncviewer`

  - Sinon, TightVNC est téléchargeable à partir de [tightvnc.com](http://www.tightvnc.com/download.php)


## Étape 3: Si nécessaire, configurer le Pi pour lui donner une adresse IP

Ceci est la méthode que vous utiliserez si votre administrateur réseau refuse de permettre à un Raspberry Pi d'être connecté au réseau principal de l'école. Ainsi, chaque Raspberry Pi sera connecter directement à un ordinateur hôte en utilisant un seul câble Ethernet, permettant ainsi un réseau complètement isolé de point à point entre les deux. 

*Remarque: vous n'avez pas besoin d'un câble croisé pour cela; un câble standard fonctionnera parce que le port Ethernet du Pi auto-commute les broches transmission et réception.*

Tout d'abord, nous aurons besoin d'installer un logiciel sur le Pi, donc pour cette première partie, vous aurez besoin de le connecter à un réseau local pour l'accès à Internet. Nous allons donner au port Ethernet le même comportement qu'un routeur domestique. Cela signifie l'attribution d'une adresse IP statique et l'installation d'un service DHCP ( `dnsmasq`) qui répondra aux demandes d'adresse de l'ordinateur hôte. 

1. En ligne de commande ou d'une fenêtre LXTerminal, tapez:

  ```
  sudo apt-get update
  sudo apt-get install dnsmasq
  ```
  
1. C'est une bonne idée d'utiliser une plage d'adresses IP qui est très différente de votre réseau principal, donc nous allons utiliser 10.0.0.X. Pour configurer cela, il faut modifier le fichier d'interface réseau. Entrez la commande suivante:

  ```
  sudo nano /etc/network/interfaces
  ```
1. Trouvez la ligne `iface eth0 inet dhcp` et ajoutez un symbole dièse au début de la ligne pour la désactiver. Puis ajoutez les quatre autres lignes indiquées ci-dessous:

  ```
  # iface eth0 inet dhcp
  auto eth0
  iface eth0 inet static
  address 10.0.0.1
  netmask 255.255.255.0
  ```
  
1. Pressez **Ctrl** et **X** suivi de **O** puis **Entrer** pour enregistrer et sortir de nano. Le Raspberry Pi va maintenant avoir une adresse statique comme `10.0.0.1`.

## Etape 4: Configurer **dnsmasq** pour donner des adresses IP

Tout d'abord, faire une sauvegarde du fichier de configuration par défaut puis sauver la mienne à sa place:

1. Tapez `cd /etc` en ligne de commande pour changer de répertoire, puis appuyez sur **Entrer**. 
1. Ensuite tapez `sudo mv dnsmasq.conf dnsmasq.default` et appuyer sur **Entrer**.
1. Puis tapez `sudo nano dnsmasq.conf` et appuyer sur **Entrer**. Vous devriez maintenant être en train de modifier un fichier vide. Tapez la commande suivante en elle:

  ```
  interface=eth0
  dhcp-range=10.0.0.2,10.0.0.250,255.255.255.0,12h
  dhcp-option=3,10.0.0.1
  ```
  La première ligne indique `dnsmasq` pour écouter les demandes DHCP sur le port Ethernet du Pi. La deuxième ligne spécifie la plage d'adresses IP qui peuvent être donnés. La troisième ligne fournit la passerelle par défaut pour l'ordinateur hôte (qui ne sera pas réellement utilisé ici).

1. Déconnectez le Pi du réseau local et redémarrez en tapant `sudo reboot`.

## Étape 5: Testez la connexion

1. Après le redémarrage de Pi, donnez-lui une minute, et vous pouvez aller de l'avant et de brancher le câble Ethernet directement du Pi à l'ordinateur hôte. L'ordinateur hôte doit alors donner une adresse IP qui sera `10.0.0.X`, où X est un nombre aléatoire compris entre 2 et 250.
1. Vérifiez qu'il ya une connexion active en ouvrant une invite de commande sur l'ordinateur hôte (un terminal sur OSX et Linux), et entrez la commande suivante `ping 10.0.0.1`.

  Si vous voyez `reply, reply, reply `alors ça fonctionne. Si vous voyez request timed out, quelque chose ne va pas et vous devez revenir en arrière et tout revérifier.

1. You can now open up your VNC viewer on the host PC and connect it to the Pi. When prompted for the remote host enter   `10.0.0.1:1` and click **connect**. It could also be `10.0.0.1:0` depending on how you set it up in step 1.

  You'll be prompted for the password that you chose during step 1; after that you'll see the Pi desktop and will be able to get going with Scratch or whatever program you need. Remember that 3D games like Minecraft are not going to work using this method, as those draw their image directly to the local screen memory and will be ignored by VNC. You'll just see an empty window.
