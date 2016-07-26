# Un guide animateur/enseignant pour l'utilisation du Raspberry Pi en classe

![](cover.png)

Si vous cherchez à vous servir des Raspberry Pis en classe, ce guide vous présente plusieurs façons de l'envisager. Certaines solutions repensent l'utilisation de l'équipement existant afin de réduire les éventuels frais.

## Démarrer avec le Raspberry Pi

Si vous ne connaissez pas déjà l'outil, avant de continuer la lecture, il vous est conseillé de commencer par [ce guide qui apprend simplement à mettre en place un Raspberry Pi](getting-started-guide.md) pour la première fois.

Une des utilisations du Raspberry Pi dans la salle de classe est comme périphérique autonome que les enfants peuvent utiliser en dehors du réseau scolaire pour créer des programmes et des projets électroniques, sans crainte de casser du matériel coûteux ou de faire sauter un réseau scolaire. C'est un environnement qui permet la liberté de l'échec, et c'est en échouant que les enfants apprennent. Si un fichier système est endommagé, vous pouvez toujours recommencer avec une nouvelle image de la carte SD. Si vous cassé une LED, cela n'a pas d'importance.

Une autre caractéristique intéressante du Raspberry Pi dans l'enseignement est qu'il intrigue, et les enfants posent des questions sur le matériel. Pourquoi est-ce un ordinateur? Comment fonctionne-t-il ? Quels sont les périphériques d'entrée et de sortie? Où stocke-t-il son logiciel? etc.

## Matériel nécessaire

![](images/Raspberry-Pis.jpg)

### De quoi aurez-vous besoin pour un parc autonome de Raspberry Pi pour la classe ?

- Plusieurs Raspberry Pi; un ou deux peuvent servir aux travaux des enfants. Un [Model B](https://www.raspberrypi.org/products/model-b/), [Model B+](https://www.raspberrypi.org/products/model-b-plus/) ou un [Raspberry Pi 2](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) conviendra pour cet exercice.
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
PINET est un système libre qui centralise les comptes d'utilisateurs et le stockage de fichiers pour les salles de classe Raspberry Pi. Avec elle, tous les Raspberry Pi se connecte à un serveur central et tout étudiant peut s'asseoir à tout Raspberry Pi dans la salle de classe et se connecter. Il a été conçu pour être incroyablement simple à installer et à utiliser pour les animateurs/enseignants. Plus de détails peuvent être trouvés sur le site [PiNet](http://pinet.org.uk/).   

## Gestion d'un set pour la classe
- [Comment faire un jeu de cartes SD pour la classe ](class-sd-cards.md)

## Compétences transversales

L'utilisation du Raspberry Pi dans une salle de classe peut également offrir différentes méthodes d'enseignement et d'apprentissage. Il ouvre la possibilité de voir l'informatique plus comme une activité créative et constructive. L'informatique peut être un sujet véritablement transdisciplinaire dans l'art, la science et la technologie. Le Raspberry Pi peut offrir plus que vous ne l'imaginez dans l'éducation.

- [A quoi ressemble une bonne classe d'informatique ? par Clive Beale](http://www.raspberrypi.org/what-does-a-good-computing-classroom-look-like)

## Ressources pédagogiques

Avec des professeurs qualifiés parmi notre personnel, nous produisons des outils d'enseignement, y compris des parcours complets d'exercices transversaux. Ils sont publiés sous une licence Creative Commons afin que les animateurs/enseignants puissent les utiliser comme bon leur semble.

- [Enseigner - Ressources pédagogiques Raspberry Pi](http://www.raspberrypi.org/resources/teach/)
- Un excellent moyen commencer est notre [Leçon de prise en main](http://www.raspberrypi.org/learning/getting-started-with-raspberry-pi-lesson/)

## Formation

Ici, à la Fondation Raspberry Pi nous offrons depuis peu de temps des formations GRATUITES pour les animateurs/enseignants à l'Académie Raspberry Pi ou Picademie. Pour en savoir plus, cliquez sur les liens ci-dessous:

- [Picademy](http://www.raspberrypi.org/picademy)

## Demander à la communauté

La Communauté Raspberry Pi est prête, volontaire et dans la plupart des cas en mesure d'aider les écoles à enseigner l'informatique avec le Raspberry Pi. Ils sont une source d'expériences et de ressources souvent inexploités . Si, après avoir lu ce guide, vous ne trouvez pas les solutions à vos problèmes en classe, alors il est recommandé de tendre la main à la communauté.

> Quand j'ai commencé à utiliser le Raspberry Pi dans ma classe à la fin 2012, les moniteurs étaient tous en VGA. A cette époque, il n'y avait pas de câble convertisseur, donc j'ai mis un message sur Twitter demandant si des entreprises locales se débarrassaient de tous leurs moniteurs DVI. Quelques minutes après, j'ai eu une réponse, et ce week-end, je collectionnais les moniteurs dont j'avais besoin gratuitement.

> La communauté Raspberry Pi est l'un des plus utiles avec laquelle j'ai été en contact. Utiliser les [forums](http://www.raspberrypi.org/forums) ou Twitter avec le hashtag `#raspberrypi` ou `#picademy` pourrait être aussi un moyen de trouver des solutions pour votre salle de classe. ~ Carrie Anne Philbin

### La page de la communauté

Sur notre site, nous vous proposons des personnes et des organisations de premier plan au sein de notre communauté qui font de l'excellent travail de sensibilisation. C'est un bon départ pour en savoir plus à propos du Raspberry Pi.
- [Page de la communauté officielle](http://www.raspberrypi.org/community/)

### Le forum

Si vous avez une question, quel que soit votre niveau ou expérience, alors vous pouvez poser une question sur notre forum. Nous avons une section éducation spécialement mis en place pour cela. C'est un forum très convivial, où quelqu'un va répondre à votre question très rapidement et poliment. Un certain nombre de nos éducateurs certifiés Raspberry Pi sont actifs sur ce forum, en répondant à des questions et partageant les bonnes expériences.
- [Section éducation du Forum](http://www.raspberrypi.org/forums/viewforum.php?f=17&sid=f9cb8df1edfa3781e9a7afa26aaa4e42)

### Licence

Sauf autres précisions, tout ce qui se trouve dans cet répertoire est couvert par la licence suivante :
![Creative Commons Attribution 4.0 International Licence](http://i.creativecommons.org/l/by-sa/4.0/88x31.png)

***Un guide animateur/enseignant pour l'utilisation du Raspberry Pi en classe (v.o. Teacher's classroom guide)*** par la [Raspberry Pi Foundation](http://www.raspberrypi.org) est crée sous une licence [Creative Commons Attribution 4.0 International Licence](http://creativecommons.org/licenses/by-sa/4.0/).

D'après un travail paru sur https://github.com/Raisin-Pi/teachers-classroom-guide fait par Lionel Warnault pour le projet [D-Clics Numériques](http://d-clicsnumeriques.org/)
