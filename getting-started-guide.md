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
1. If you intend to connect your Raspberry Pi to the internet, plug in an Ethernet cable into the Ethernet port next to the USB ports; if you do not need an internet connection, skip this step.
1. Finally, when you are happy that you have plugged in all the cables and SD card required, plug in the micro USB power supply. This action will turn on and boot your Raspberry Pi.
1. If this is the first time your Raspberry Pi and NOOBS SD card have been used, then you will have to select an operating system and configure it. [Follow the NOOBS guide to do this](http://www.raspberrypi.org/help/noobs-setup/).

## Step 3: Logging into your Raspberry Pi

Hurrah, Raspbian has loaded, your Raspberry Pi is up and running... now what? Let's log in to find out:

1. Once your Raspberry Pi has completed the boot process, a login prompt will appear. The default login for Raspbian is username `pi` with the password `raspberry`. Note you will not see any writing appear when you type the password. This is a security feature in Linux.
1. After you have successfully logged in, you will see the command line prompt `pi@raspberrypi~$`.
1. To load the graphical user interface, type `startx` and press **Enter** on your keyboard.
	
	
## What next?

If you are new to using Linux, then you may wish to learn a little about how to use commands to navigate around your Raspberry Pi, create files, and run applications using simple text.

Then it's time to get learning or making using our [Raspberry Pi Learning Resources here](http://www.raspberrypi.org/resources/).

