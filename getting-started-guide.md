# Débuter avec le Raspberry Pi

Vous avez un Raspberry Pi, félicitations! Je suis sûr que vous brûler d'envie de commencer à créer vos propres projets. Alors qu'attendez vous ? Suivez toutes les étapes ci-dessous.

## Etape 1: Assurez-vous que vous avez tout ce dont vous avez besoin

Avant de commencer, vérifiez que vous avez toutes les pièces dont vous avez besoin:

### Elements requis :

- Un Raspberry Pi (soit un [Model B](http://www.raspberrypi.org/product/model-b/) ou un  [Model B+](http://www.raspberrypi.org/product/model-b-plus/))

	![](images/Raspberry-Pis.jpg)

- Carte SD
	- Nous recommandons une carte SD de 8GB class 4, avec idéalement NOOBS préinstallé. 
	- Vous pouvez [acheter une carte avec NOOBS préinstallé](http://swag.raspberrypi.org/collections/frontpage/products/noobs-8gb-sd-card), ou vous pouvez le télécharger gratuitement depuis [notre page de téléchargement](http://www.raspberrypi.org/downloads/).
	
- Affichage et connectique :
	- Tout moniteur HDMI/DVI ou TV devrait fonctionner comme écran pour le Pi. 
	- Pour un meilleur rendu, utilisez en un avec une entrée HDMI, mais d'autres connexions sont possibles pour les anciens écrans. 
	
- Clavier et souris
	- Tout clavier et souris USB standard fonctionnera avec votre Raspberry Pi.
	
- Alimentation
	- Utilisez [une alimentation de 5V micro USB](http://swag.raspberrypi.org/collections/pi-kits/products/raspberry-pi-universal-power-supply) pour votre Raspberry Pi. Veillez à ce que quel que soit l'alimentation que vous utilisez, les sorties soient au moins de 5V.; une puissance insuffisante entraînera un disfonctionnement de votre Pi.

Vous pouvez acheter un kit à partir du magasin Swag Raspberry Pi pour vous aidez à démarrer [ici](http://swag.raspberrypi.org/collections/frontpage/products/b-raspberry-pi-starter-kit).

### Pas indispensable mais utile à avoir:

- Connection internet
	- Pour mettre à jour ou télécharger le logiciel, nous vous recommandons de connecter votre Raspberry Pi à internet via un câble Ethernet ou un adaptateur WiFi.
	- Si vous avez un adaptateur WiFi, consulter notre [guide d'installation WiFi  ici](http://www.raspberrypi.org/documentation/configuration/wireless/README.md).

- Son
	- Casques, écouteurs ou haut-parleurs avec un jack 3,5 mm fonctionnent avec votre Raspberry Pi.

	
## Etape 2: Connectez votre Raspberry Pi

Maintenant, vous avez toutes les pièces dont vous avez besoin pour commencer, nous allons commencer à assembler !

1. Commencez par insérer votre carte SD dans la fente pour carte SD sur le Raspberry Pi, dans le bon sens. * Notez que le logiciel NOOBS devrait déjà être sur cette carte. S'il ne l'est pas, suivez le [guide NOOBS  ici](http://www.raspberrypi.org/help/noobs-setup/).*
1. Ensuite, branchez votre clavier et une souris USB dans les ports USB sur le Raspberry Pi. Assurez-vous que votre moniteur ou votre téléviseur soit allumé, et que vous avez sélectionné la bonne entrée (par exemple 1 HDMI, DVI, etc).
1. Ensuite, connectez le câble HDMI de votre Raspberry Pi à votre moniteur ou téléviseur.
1. Si vous avez l'intention de connecter votre Raspberry Pi à Internet, branchez un câble Ethernet dans le port Ethernet à côté des ports USB; si vous n'avez pas besoin d'une connexion Internet, ignorez cette étape.
1. Enfin, quand vous êtes heureux d'avoir branché la carte SD et tous les câbles  nécessaires, branchez l'alimentation micro-USB. Cette action allumera et démarrera votre Raspberry Pi.
1. Si c'est la première fois que votre Raspberry Pi et NOOBS sont utilisés, vous devez sélectionner un système d'exploitation et le configurer. [Suivez le guide NOOBS pour cela](http://www.raspberrypi.org/help/noobs-setup/).

## Etape 3: Connexion à votre Raspberry Pi

Hourra, Raspbian est chargé, votre Raspberry Pi est en marche ... et maintenant? Nous allons ouvrir une session pour le découvrir:

1. Une fois que votre Raspberry Pi a terminé le processus de démarrage, une invite de connexion apparaît. La connexion par défaut pour Raspbian est le nom d'utilisateur `pi` avec le mot de passe `raspberry`. Notez que vous ne verrez pas les caractères apparaître lorsque vous tapez le mot de passe. Ceci est une caractéristique de sécurité dans Linux.
1. Après s'être connecté avec succès, vous verrez l'invite de ligne de commande `pi@raspberrypi~$`.
1. Pour charger l'interface graphique, tapez `startx` et appuyez sur **Enter** sur votre clavier.
	
	
## What next?

If you are new to using Linux, then you may wish to learn a little about how to use commands to navigate around your Raspberry Pi, create files, and run applications using simple text.

Then it's time to get learning or making using our [Raspberry Pi Learning Resources here](http://www.raspberrypi.org/resources/).

