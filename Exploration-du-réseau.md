# Chapitre 1 : Exploration du réseau

## Connecté au monde entier

Aujourd'hui, la communication rapide et efficace est très importante dans notre société. Son évolution fut rapide et de grandes choses sont encore à venir permettant ainsi d'abolir les frontières géographiques.

Il existe tous types de réseaux qu'ils soient humains ou informatiques. Les réseaux sont alors utiles pour partager et opérer à l'echelle personnelle mais aussi à l'echelle de l'entreprise.

Aujourd'hui on utilise le réseau informatique pour de multiples usages, on le nomme donc réseau convergé.

## Clients et serveurs

Tous les ordinateurs et machines utilisant le réseau sont des hôtes (aussi appelés périphériques finaux). Les serveurs sont des logiciels qui mettent a disposition leurs services. Les clients sont des logiciels permettant de demander des informations aux serveurs pour qu'elles soient utilisés par l'utilisateur.

> Exemple: Un serveur Web permet de mettre a disposition sur le réseau, des pages web obtenues via HTTP. Firefox ou Google Chrome sont des clients qui vont contacter le serveur pour obtenir la page demandée.

### Peer to peer

Il peut arriver qu'un hôte tienne tienne à la fois le rôle de client et de serveur, ainsi chaque hôte peut recevoir et transmettre l'information. On apelle ce réseau un réseau peer to peer.

**Avantages**

* Facile à configurer
* Moins de compléxité
* Cout inférieur
* Utilisable pour des tâches simples comme le transfert de fichiers

**Inconvénients**

* Pas d'administration centralisée
* Peu de sécurité
* Non évolutif
* Performances ralenties

## Composants réseaux

La structure d'un réseau est composée de 3 grandes parties:

* Les appareils
* Les supports
* Les services

Les périphériques sont reliés entre eux au travers d'une carte réseau permettant d'encoder ou de décoder les données sur le réseau. Ces cartes réseaux sont en contact avec un support de communication par l'intermédiaire d'une interface représentant un port physique.

### Les périphériques finaux

Les machines qui reçoivent et envoient des données. Cela peuvent être des machines hébergeant des serveurs ou des clients.

> Exemples : Ordinateur, Téléphone IP, Imprimante

### Périphériques réseaux

Des machines permettant de correctement transmettre les données sur le réseau. Ils utilisent les adresse d'emission et de réception pour transmettre les paquets au bon endroit. Il permettent les opérations suivantes :

* Régénérer et retransmettre les signaux réseaux
* Gérer des informations indiquant les chemins qui existent à travers le réseau
* Indiquer aux autres périphériques les erreurs de communication
* Diriger des données vers d'autres chemins en cas d'échec de liaison
* Classifier et diriger les messages en fonction des priorités
* Autoriser ou refuser le flux de données selon les paramètres de sécurité

### Support

Le support fournis le canal sur lequel se déplace le signal représentant les paquets. Le support peut etre de 3 types différents:

* Fil métalique (cuivre) les données transitent sous forme élécrique
* Fibre de verre ou plastique (fibre optique) les données sont sous forme de lumière
* Sans fil les données sont codées suivant une longueur d'onde éléctromagnetique

On choisis le type de support à utiliser en fonction de :

* La distance maximale sur laquelle les supports peuvent transporter le signal
* L'environnement dans lequel les supports sont installés
* La quantité de données a transporter
* Le coût envisageable pour l'installation

## Types de réseau

les inftrastructures réseaux peuvent varier en fonction de :

* La taille de la zone couverte
* Le nombre d'utilisateurs
* Les services disponibles

Parmis les infrastructures principales on trouve : 

* **LAN (Local Area Network) ou réseau local** Un réseau peu étendu géographiquement, le plus souvent un réseau de petite entreprise ou domestique. Ce réseau permet une grande bande passante
* **WAN (Wide Area Network) ou réseau étendu** Un réseau de taille plus importante géorgraphiquement géré per un prestataire réseau.
* **MAN (Metropolitan Area Network) ou réseau intermédiaire** Réseau d'une grande entreprise plus grande qu'un LAN mais plus petite qu'un WAN
* **WLAN (Wireless LAN) ou réseau sans fil** Un réseau similaire au LAN mais sans fil
* **SAN (Storage Area Network) ou réseau de stockage** Réseau permettant la transmission de fichiers et la sauvegarde de ceux-ci

### Internet

Internet est un ensemble de réseaux WAN permettenat d'interconnecter une grande partie de la planète. Internet n'est pas détenu par une personne mais chacun des réseaux y participe.

### Intranet & extranet

Le terme intranet fait référence a un réseau de taille réduite appartenant à une entreprise ou à une organisation.

L'extranet est un service réseau fourni par une entreprise ou une organisation pour permettre d'interagir avec elle de l'exterieur de son réseau LAN ou MAN.

### Accès a internet

L'accès a internet peut s'effectuer par plusieurs supports : 

* **DSL** On utilise le réseau téléphonique avec la téchnologie DSL pour transmettre les données
* **Câble** On se connecte directement au réseau par un câble spécifique
* **Cellulaire** On utilise un signal sans fil téléphonique pour communiquer sur le réseau
* **Satellite** On se connecte au réseau par l'intermédiaire d'un satellite, plus utile dans les régions reculées
* **Ligne commutée** Une connexion à faible débit 

## Archithectures de réseaux

Les réseaux permettant aujourd'hui de relier tout les types de médias qu'ils soient destinés à la diffusion, au téléphone ou à la transmission de données informatiques doivent être :

* Tolérents aux pannes : Le réseau doit toujours être disponible malgré la panne d'un élément de celui-ci
* Évolutifs : Permettant de s'agrandir rapidement pour accueillir de nouveaux périphériques
* Qualitatifs : Permettant d'optimiser les transferts pour obtenir un débit le plus élevé possible
* Sécurisés : Permettant de conserver la confidentialité, l'intégrité et la disponibilité des échanges

## Expansion des usages

Aujourd'hui, on remarque une augmentation des usages d'internet au quotidien sur de nombreux nouveaux usages : 

* **BYOD (Bring Your Own Device)** On laisse la possibilité à l'utilisateur d'utiliser le périphérique final qu'il désire pour se connecter au réseau
* **Collaboration en ligne**
* **Communication vidéo**
* **Cloud computing** Permettant de stocker une masse de données sur internet sans avoir besoin de mobiliser sa propre équipe ou ses propres équipements

On utilise aussi de nouveau moyens de connecter les appreils finaux : 

* **Courant porteur** Les câbles domestiques d'alimentation sont utilisés pour transmettre des données
* **Haut débit sans fil** Utilisant la technologie cellulaire

## Sécurité

La sécurité d'un réseau est primordiale et on doit mettre en place des systèmes permettant d'empêcher toutes les menaces exterieures :

* **Virus, vers et cheval de troie** Des logiciels executant du code malveillant sur le périphérique utilisateur
* **Spyware ou Adware** Des logiciels qui collectent des données sur le système utilisateur
* **Zero day** Attaques le jour de la détection de la vulnérabilité
* **Attaque pirate** Attaques effectuée par une personne ayant de solides conaissances du réseau
* **Vol de données**
* **Usurpation d'identitée**

Il n'existe pas de solution maîtresse permettant de sécuriser un réseau mais on peut mettre en place un ensemble de solutions :

* Installer des antivirus et anti-logiciels espions
* Installer un pare-feu visant à filtrer les données qui entrent et sortent du réseau
* Préciser les accès de chaque personne aux ressources du réseau
* Des réseaux privés virtuels permettant un accès sécurisé hors du réseau LAN
