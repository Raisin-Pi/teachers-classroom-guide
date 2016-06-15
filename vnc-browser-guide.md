# Contrôle à distance d'un Raspberry Pi via votre navigateur web 

Ce guide est une légère variante de l'utilisation de bureau à distance, tels que VNC, pour se connecter à un Raspberry Pi. 

Le principe de base est d'utiliser un autre ordinateur que la console d'entrée pour le Raspberry Pi sans avoir besoin d'un écran, d'un clavier et d'une souris connecté au Pi. C'est l'idéal si, par exemple, vous avez une salle pleine d'ordinateurs portables, Chromebooks ou iMacs.

Cela diffère de la méthode précédente en ce que vous ne devez pas installer un logiciel sur l'ordinateur hôte / ordinateur portable. Vous pouvez régler le Raspberry Pi afin qu'il fournisse tout ce dont l'ordinateur hôte a besoin via le navigateur web. Cela devient aussi facile que de taper une adresse.

Voici un exemple du produit final sur Windows / IE:

![](images/vnc_ie.png)

## Que faut-il faire ?

Ce système fonctionne sur tous les navigateurs web compatible HTML5, notamment ces versions de navigateur ou plus récente:

- Chrome 8
- Firefox 4
- Safari 5
- iOS Safari 4.2
- Opera 11
- IE 9

## Etape 1: Configuration du serveur sur un Raspberry Pi

1. Commencez avec une nouvelle installation de Raspbian et connectez-vous en tant qu'utilisateur "pi" par défaut. Vous pouvez utiliser l'interface de ligne de commande pour ce guide.
1. Installez les paquets suivants (tightvncserver et screen).Exécuter ces commandes à partir du terminal:

	```
	sudo apt-get update
	sudo apt-get install tightvncserver screen -y
	```

1. Ensuite, exécutez TightVNC Server, qui vous invite à entrer un mot de passe et une option de visiualisation du mot de passe , en tapant `tightvncserver` et appuyer sur **Entrer** sur le clavier.

1. Maintenant, nous allons le client VNC HTML5. Entrez les commandes suivantes et appuyez sur "Entrée" à la fin de chaque ligne:

	```
	cd /usr/local/share/
	sudo git clone git://github.com/kanaka/noVNC
	```

1. Nous avons juste besoin de faire un petit ajustement de certains des fichiers.  Le dossier que nous venons de téléchargé sera utilisé comme racine HTTP pour le Pi, donc nous avons juste besoin de nous assurer qu'il y a bien une page index. Cela permettra à l'ordinateur hôte d'accéder au logiciel client VNC.
	
	```
	cd noVNC
	sudo cp vnc_auto.html index.html
	```

1. Ensuite, nous devons tout régler pour démarrer automatiquement, puisque vous allez probablement vouloir utiliser le Raspberry Pi en mode sans tête (sans clavier, souris ou moniteur). Pour ce faire, nous avons besoin de télécharger quelques scripts pour `init.d`. Entrez les commandes suivantes:

	```
	cd /etc/init.d/
	sudo wget https://raw.githubusercontent.com/raspberrypilearning/teachers-classroom-guide/master/vncboot --no-check-certificate
	sudo nano vncboot
	```

	*Notez la ligne qui dit `-geometry 1280x800` . Ceci définit la résolution de l'écran pour le bureau à distance, de sorte que vous pouvez le modifier en fonction de la taille de l'écran de l'ordinateur hôte. Idéalement, cela devrait être réglé légèrement inférieur pour éviter d'avoir des barres de défilement.*

1. Appuyez sur "Ctrl" et "O" suivie par "Entrer" pour sauver, puis "Ctrl" et "X" pour quitter.

1. Le script que vous venez de créer fait de VNC une partie des services d'arrière-plan que Linux contrôle. Nous avons ensuite besoin d'enregistrer le script. Entrez les commandes suivantes:

	```
	sudo chmod 755 vncboot
	sudo update-rc.d vncboot defaults
	```

	Ignorez les messages sur les balises LSB manquantes et continuez. La partie serveur est faite. Ensuite, nous devons mettre en place un script similaire pour le client HTML5.

## Étape 2: Configuration du client

Avec le côté serveur terminée, vous devez maintenant télécharger un script similaire pour le client HTML5.

1. Entrez la commande suivante:

	```
	sudo wget https://raw.githubusercontent.com/raspberrypilearning/teachers-classroom-guide/master/vncproxy --no-check-certificate
	```

1. Enregistrer ce script avec Linux en tapant:

	```
	sudo chmod 755 vncproxy 
	sudo update-rc.d vncproxy defaults 98
	```
	
	Ignorez les messages sur les balises LSB manquantes et continuez.

1. Maintenant, redémarrez votre Raspberry Pi en tapant `sudo reboot` et les services démarreront automatiquement. Lorsque le Pi a redémarré, vous devriez maintenant être en mesure d'entrer l'adresse IP du Raspberry Pi dans le navigateur Web de l'ordinateur hôte. Vous serez invité à entrer le mot de passe que vous avez spécifié lors de la configuration du serveur VNC.

	*Note: une erreur a parfois été observée sur la première fois que vous essayez de vous connecter; cela peut-être causé par le proxy qui démarre avant que le socket serveur VNC soit ouvert. Si vous voyez ceci la barre supérieure devient rouge. Rafraîchisser juste en appuyant sur (F5), entrez le mot de passe à nouveau et cela devrait fonctionner.*

## Étape 3: Mode maître et esclave

Il y a un autre truc que vous pouvez faire ici si vous souhaitez affiner la configuration par la suite. 

En utilisant les instructions suivantes, chaque Raspberry Pi sera directement connecté à l'ordinateur hôte à l'aide d'un seul câble Ethernet, permettant ainsi un réseau complètement isolé de point à point entre les deux; De cette façon, vos administrateurs réseau ne devraient pas avoir à se plaindre. Notez que vous n'avez pas besoin d'un câble croisé pour cela; un câble standard fonctionnera, parce que le port Ethernet du Pi auto-commute les broches transmission et réception.

Tout d'abord, nous aurons besoin d'installer un logiciel de plus sur le Pi. Nous allons rendre le port Ethernet Pi similaire à un routeur domestique. Cela signifie l'attribution d'une adresse IP statique et l'installation d'un service DHCP (dnsmasq) qui répondra aux demandes d'adresse de l'ordinateur hôte.

1. Entrez les commandes suivantes:

	```
	sudo apt-get install dnsmasq -y
	```

1. C'est une bonne idée d'utiliser une plage d'adresses IP qui est très différent de votre réseau principal, donc nous allons utiliser `10.0.0.X`. Pour configurer cela, il faut modifier le fichier d'interface de réseau. Entrez la commande suivante:

	```
	sudo nano /etc/network/interfaces
	```

1. Trouvez la ligne suivante `iface eth0 inet dhcp`, ajouter un symbole dièze au début de la ligne pour la désactiver, puis ajouter les quatre lignes indiquées ci-dessous.

	```
	# iface eth0 inet dhcp
	auto eth0
	iface eth0 inet static
	address 10.0.0.1
	netmask 255.255.255.0
	```

1. Appuyez sur "Ctrl" et "O" suivie par "Entrer" pour sauver, puis "Ctrl" et "X" pour quitter. Le Raspberry Pi va maintenant avoir une adresse statique `10.0.0.1`.

1. Ensuite configurez `dnsmasq` (Que vous avez installé précédemment) pour donner des adresses IP. Nous allons créér un fichier de configuration pour le service `dnsmasq`, donc nous allons faire d'abord une sauvegarde du fichier de configuration par défaut puis enregistrez le notre à sa place:

	```
	cd /etc
	sudo mv dnsmasq.conf dnsmasq.default
	sudo nano dnsmasq.conf
	```

1. Vous devriez maintenant être en train d'éditer un fichier vide. Tapez la commande suivante en elle:

	```
	interface=eth0
	dhcp-range=10.0.0.2,10.0.0.250,255.255.255.0,12h
	dhcp-option=3,10.0.0.1
	dhcp-option=6,10.0.0.1
	```

	La première ligne dit à `dnsmasq` d'écouter les demandes DHCP sur le port Ethernet du Pi. La deuxième ligne spécifie la plage d'adresses IP qui peuvent être donnés. Les troisième et quatrième lignes indiquent à l'ordinateur hôte les paramètres de la passerelle par défaut et du serveur DNS.

1. Ensuite, faire une petite modification du fichier hosts. Cela permettra à l'utilisateur de taper 'pi' dans le navigateur au lieu de `10.0.0.1`.Entrez ce qui suit pour modifier le fichier hosts: `sudo nano /etc/hosts`.

1. Trouvez la ligne qui dit `127.0.0.1		raspberrypi` et ajoutez la ligne suivante:

	`10.0.0.1		pi`

1. Appuyez sur "Ctrl" et "O" suivie par "Entrer" pour sauver, puis "Ctrl" et "X" pour quitter. Ensuite, débranchez le Pi du réseau local et redémarrez en tapant `sudo reboot`.

1. Vous pouvez continuer et branchez le câble Ethernet directement du Pi à l'ordinateur hôte.
L'ordinateur hôte doit alors donner une adresse IP qui sera 10.0.0.x, où X est un nombre aléatoire entre 2 et 250.

Essayer d'ouvrir une invite de commande sur l'ordinateur hôte (un terminal sur OSX et Linux), et entrez la commande suivante:

```
ping 10.0.0.1
```

Si vous voyez `reply, reply, reply` alors ça fonctionne. Si vous voyez request time out, alors quelque chose ne va pas et vous aurez besoin de revenir en arrière et tout revérifier.

Vous devriez maintenant être en mesure d'ouvrir un navigateur Web sur l'ordinateur hôte et entrez `pi` dans la barre d'adresse pour accéder à la page de client VNC. 

*Note: Windows users:* This may not work properly on Windows (you'll still need to use `10.0.0.1`), but if you install a package called `winbind` you'll be able to type the Raspberry Pi hostname into the browser. Usually the hostname is `raspberrypi`. The `winbind` package can be installed with the command below:

`sudo apt-get install winbind`

However, it should be fine on OSX, Ubuntu, and any other flavour of Linux.

![](images/vnc_firefox.png)

You will be prompted for the password that you specified when setting up the VNC server.

*Note: an error has occasionally been observed on the first time that you try to connect; this is possibly caused by the proxy starting before the VNC server socket is open. If you see this the top bar goes red. Just hit refresh (F5), enter the password again and it should work.*
