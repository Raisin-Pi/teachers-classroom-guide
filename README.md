# Un guide enseignant pour l'utilisation du Raspberry Pi en classe

![](cover.png)

Si vous cherchez à vous servir des Raspberry Pis en classe, ce guide vous présente plusieurs façons de l'envisager. Certaines solutions repensent l'utilisation de l'équipement existant afin de réduire les éventuels frais.

## Démarrer avec le Raspberry Pi

Si vous ne connaissez pas déjà l'outil, avant de continuer la lecture, il vous est conseillé de commencer par [ce guide qui apprend simplement à mettre en place un Raspberry Pi](getting-started-guide.md) pour la première fois.

Une des utilisations du Raspberry Pi dans la salle de classe est comme périphérique autonome que les élèves peuvent utiliser en dehors du réseau scolaire pour créer des programmes et des projets électroniques, sans crainte de casser du matériel coûteux ou de faire sauter un réseau scolaire. C'est un environnement qui permet la liberté de l'échec, et c'est en échouant que les élèves apprennent. Si un fichier système est endommagé, vous pouvez toujours recommencer avec une nouvelle image de la carte SD. Si vous cassé une LED, cela n'a pas d'importance.

Une autre caractéristique intéressante du Raspberry Pi dans l'enseignement est qu'il intrigue, et les élèves posent des questions sur le matériel. Pourquoi est-ce un ordinateur? Comment fonctionne-t-il ? Quels sont les périphériques d'entrée et de sortie? Où stocke-t-il son logiciel? etc.

## Matériel nécessaire

![](images/Raspberry-Pis.jpg)

### De quoi aurez-vous besoin pour un parc autonome de Raspberry Pi pour la classe ?

- Plusieurs Raspberry Pi; un ou deux peuvent servir aux travaux des élèves. Un [Model B](https://www.raspberrypi.org/products/model-b/), [Model B+](https://www.raspberrypi.org/products/model-b-plus/) ou un [Raspberry Pi 2](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) conviendra pour cet exercice.
- Suffisament de [cartes SD (Model B) ou de cartes microSD ](http://swag.raspberrypi.org/collections/frontpage/products/noobs-8gb-sd-card) (Model B+ et Pi 2) pour chaque Pi.
- Claviers et souris USB pour chaque Pi.
- [Alimentation Micro USB](http://swag.raspberrypi.org/collections/pi-kits/products/raspberry-pi-universal-power-supply) pour chaque Pi.
- Des câbles HDMI pour se connecter à un moniteur pour chaque Pi (voir les solutions pour moniteur  ci-dessous).
- Un moniteur pour chaque Pi.

### D'autres éléments dont vous aurez besoin pour un ensemble de classe Raspberry Pi en réseau.

- Une connection par câbles Ethernet
- Ou un dongle WiFi (comme celui-ci](http://thepihut.com/products/usb-wifi-adapter-for-the-raspberry-pi) de [The Pi Hut](http://thepihut.com/))

### Accessoires en option

- Un [Hubs USB](http://thepihut.com/products/7-port-usb-hub-for-the-raspberry-pi) peut être utilisé pour alimenter plus d'un Raspberry Pi et fournir des ports USB supplémentaires.
- Un duplicateur de carte SD pour copier des images de la carte SD sur plusieurs cartes. C'est utile pour faire un kit pour la classe. Malheureusement, ils coûtent 500 £ ou plus.

## Solutions pour moniteur

You could use existing school monitors with Raspberry Pis. You will need to check the cables to see if they have the correct connectors for the Pi.

- **HDMI** The Raspberry Pi outputs through a HDMI connector to a TV or monitor. Most modern TVs, monitors, and projectors use HDMI. However this is not always the case in classrooms, where technology is a few years older.

  ![](images/HDMI-Connector.jpg)

- **DVI** If the monitors in your classroom do not have a HDMI connector, but have a DVI connector, then you can purchase HDMI to DVI cables. This is an additional cost, but these cables are relatively inexpensive and replace the need for HDMI cables.

  ![](images/Dvi-cable.jpg)

- **VGA** If you have equipment that is more than a few years old, then it is likely that the monitors will have VGA connectors. In this case you will need to get a VGA adaptor for the Raspberry Pi at an additional cost. It is recommended that before you make this choice you consider some of the solutions below for using the school network to connect to the Pis instead.

  ![](images/Vga-cable.jpg)

## Networked solutions

You or your network administrators may wish to integrate Raspberry Pis more permanently into the school network. This is often a way to use existing hardware to connect to a Raspberry Pi, negating the need for extra monitors. Below are a number of ways of connecting to a Raspberry Pi using remote desktop software such as VNC and details on using PiNet as a solution to user accounts, shared folders and SD card problems.

### Remote Desktop from classroom computers to Raspberry Pis

- [Using VNC to connect to a Raspberry Pi from a desktop computer](vnc-classroom-guide.md)
- [Using VNC through a browser window](vnc-browser-guide.md)

### PiNet
PiNet is a free centralised user accounts and file storage system for Raspberry Pi classrooms. With it, all Raspberry Pis load off a central server and any student can sit down at any Raspberry Pi in the classroom and login. It was designed to be incredibly easy for teachers to setup and use. More details can be found on the [PiNet website](http://pinet.org.uk/).   

## Managing a class set
- [How to make a class set of SD cards](class-sd-cards.md)

## Cross-curricular opportunities

Using Raspberry Pis in a classroom can also offer different ways of teaching and learning. It opens up the possibility of seeing computing more as a creative and maker-style activity. Computing can be a truly cross-curricular subject in Art, Science and Technology. Raspberry Pi can offer more than you realise in education.

- [What does a good computing classroom look like? By Clive Beale](http://www.raspberrypi.org/what-does-a-good-computing-classroom-look-like)

## Teaching resources

With qualified teachers among our staff we are producing teaching materials, including full schemes of work that are cross-curricular, engaging, and satisfy the curriculum. They are published under a Creative Commons licence so that teachers can use them however they see fit.

- [Teach - Raspberry Pi Teaching Resources](http://www.raspberrypi.org/resources/teach/)
- A great place to start is with our [Getting Started Lesson](http://www.raspberrypi.org/learning/getting-started-with-raspberry-pi-lesson/)

## Training

Here at the Raspberry Pi Foundation we offer FREE CPD for teachers as the Raspberry Pi Academy or Picademy for short. To find out more click on the links below:

- [Picademy Page](http://www.raspberrypi.org/picademy)

## Asking the community

The Raspberry Pi Community is ready, willing and in most cases able to help schools teach Computing with Raspberry Pis. They are an often untapped source of experience and resources. If, after reading through this guide, you still cannot find solutions to your classroom problems, then it is recommended that you reach out to the community.

> When I started to use Raspberry Pis in my classroom in late 2012, the monitors were all VGA. At that time there was not a converter cable guaranteed to work, so I put a message out on Twitter asking if any local businesses were getting rid of any DVI monitors. Within a couple of minutes I had a response, and that weekend I collected the monitors I needed for free.

> The Raspberry Pi community is one of the most helpful I've ever been in contact with as a teacher. Using the [forums](http://www.raspberrypi.org/forums) or Twitter with the hashtag `#raspberrypi` or `#picademy` could be a way to find solutions for your classroom too. ~ Carrie Anne Philbin

### The community page

On our website we feature prominent people and organisations within our community who are doing great outreach work. It is a good starting point to learn more about Raspberry Pi.
- [Official Community Page](http://www.raspberrypi.org/community/)

### The forum

If you have a question, whatever your level or experience, then you can ask it on our forum. We have an education section especially set up for this. It is an extremely friendly forum, where someone will answer your question very quickly and politely. A number of our Raspberry Pi Certified Educators are active on this forum, helping to answer questions and share good practice.
- [Education Section of Forum](http://www.raspberrypi.org/forums/viewforum.php?f=17&sid=f9cb8df1edfa3781e9a7afa26aaa4e42)
