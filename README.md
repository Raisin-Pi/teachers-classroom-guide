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

Vous pouvez utiliser les moniteurs de l'école avec le Raspberry Pi. Vous aurez besoin de vérifier les câbles pour voir si ils ont les connecteurs appropriés pour le Pi.

- **HDMI** La sortie du Raspberry Pi via un câble HDMI reliée à un téléviseur ou un moniteur. La plupart des téléviseurs modernes, les moniteurs et projecteurs utilisent le HDMI. Cependant, ce n'est pas toujours le cas dans les salles de classe, où la technologie est un peu plus ancienne.

  ![](images/HDMI-Connector.jpg)

- **DVI** Si les moniteurs de votre salle de classe ne disposent pas d'un connecteur HDMI, mais d'un connecteur DVI, vous pouvez acheter des câbles HDMI DVI. C'est un coût supplémentaire, mais ces câbles sont relativement peu coûteux.

  ![](images/Dvi-cable.jpg)

- **VGA** Si vous avez du matériel plus anciens, alors il est probable que les moniteurs soient dotés de connecteurs VGA. Dans ce cas, vous aurez besoin d'un adaptateur VGA. Il est recommandé avant de faire ce choix d'essayez certaines des solutions ci-dessous, comme l'utilisation du réseau scolaire afin de se connecter au Pis.

  ![](images/Vga-cable.jpg)

## Solutions en reseaux

Vous ou vos administrateurs réseau peuvent intégrer le Raspberry Pi de façon plus permanente dans le réseau scolaire. C'est une façon d'utiliser le matériel existant pour se connecter à un Raspberry Pi, évitant la nécessité de moniteurs supplémentaires. Voici un certain nombre de façons de se connecter à un Raspberry Pi en utilisant un logiciel de bureau à distance tels que VNC et les détails sur l'utilisation de PINET comme solution pour gérer les comptes utilisateurs, les dossiers partagés et les problèmes de carte SD.

### Bureau à distance à partir des ordinateurs de la  classe vers les Raspberry Pis

- [Utilisation de VNC pour se connecter à un Raspberry Pi à partir d'un ordinateur de bureau](vnc-classroom-guide.md)
- [Utilisation de VNC par une fenêtre de navigateur](vnc-browser-guide.md)

### PiNet
PINET est un système libre qui centralise les comptes d'utilisateurs et le stockage de fichiers pour les salles de classe Raspberry Pi. Avec elle, tous les Raspberry Pi se connecte à un serveur central et tout étudiant peut s'asseoir à tout Raspberry Pi dans la salle de classe et se connecter. Il a été conçu pour être incroyablement simple à installer et à utiliser pour les enseignants. Plus de détails peuvent être trouvés sur le site [PiNet](http://pinet.org.uk/).   

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
