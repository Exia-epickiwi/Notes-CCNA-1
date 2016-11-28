# Exploration du réseau

## Connecté au monde entier

Aujourd'hui, la communication rapide et éfficace est tres importante dans notre société. Son évolution fut rapide et de grandes choses sont encore à venir permettant ainsi d'bolir les frontières géographiques.

Il existe tout types de réseaux qu'ils soient humain ou informatiques. Les réseau sont alors utiles pour partager et opérer à l'echelle personnel mais aussi à l'echelle de l'entreprise.

## Clients et serveurs

Tout les ordinateurs et machines utilisant le réseau sont des hotes (aussi appelés périphériques finaux). Les serveurs sont logiciels qui mettent a disposition leurs services. les clients sont des logiciels permettant de demander des informations aux serveurs pour les qu'elles soient utilisés par l'utilisateur.

> Exemple: Un serveur Web permet de mettre a disposition sur le réseau, des pages web obtenus via HTTP. Firefox ou Google Chrome sont des clients qui vont contacter le serveur pour obtenir la page demandée.

### Peer to peer

Il peut arriver qu'un hote tienne le rôle de client et de serveur à la fois, ainsi chacun des hotes peuvent recevoir et transmettre l'information. On apelle ce réseau un réseau peer to peer.

**Avantages**

* Facile à configurer
* Moins de compléxitée
* Cout inférieur
* Utilisable pour des têches simples comme le transfert de fichiers

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

Ces périphériques sont reliés entre eux au travers d'une carte réseau permettant d'encoder ou de décoder les données sur le réseau. Ces cartes réseaux sont en contact avec un support de communication par l'intermédière d'une interface représentant un port physique.

### Les périphériques finaux

Les machines qui réçoinvent et envoient des données. Cela peut etre des machines hebergant des serveurs ou des clients.

> Exemples : Ordinateur, Téléphone IP, Imprimante

### Périphériques réseaux

Des machines permettant de correctement transmettre les données sur le réseau. Ils utilisent les adresse d'emission et de résception pour transmettre les paquets au bon endroit. Il permettent les opérations suivantes

* Régénérer et retransmettre les sigeaux réseau
* Gérer des informations indiquant les chemins qui existent à travers le réseau
* Indiquer aux autres périphériques les érreurs de communication
* Diriger des données vers d'autres chemins en cas d'echec de liaison
* Classifier et diriger les messages en fonction des priorités
* Autoriser ou refuser le flux de données selon les paramètres de sécurité

### Support

Le support fournis le canal sur lequel se déplace le signal représentant les paquets. Le support peut etre de 3 types différents:

* Fil métalique (cuivre) les données transitent sous forme élécrique
* Fibre de verre ou plastique (fibre optique) les données sont sous forme de lumière
* Sans fil les données sont codées suivant une longueure d'onde éléctromagnetique

On choisis le type de support à utiliser en fonction de :

* La distance maximale sur laquelle les supports peuvent transporter le signal
* L'environnement dans lequel les supports sont installés
* la quantitée de données a transporter
* le cout envisageable pour l'installation

## Types de réseau

les inftrastructures réseaux peuvent varier en fonction de :

* La taille de la zone couverte
* Le nombre d'utilisateurs
* Les services disponibles

Parmis les infrastructures principales on trouve : 

* **LAN (local area network) ou réseau local** Un réseau peu étendu géographiquement, le plus souvent un réseau de petite entreprise ou domestique. Ce réseau permet une grande bande passante
* **WAN (Wide Area Network) ou réseau étendu** Un réseau de taille plus importante géorgraphiquement gèré per un préstataire réseau.
* **MAN (réseau intermédière)** Réseau d'une grande entreprise plus grande qu'un LAN maius plus petite qu'un WAN
* **WLAN (réseau sans fil)** Un réseau similaire au LAN mais san fil
* **SAN (réseau de stockage)** Réseau permettant la transmission de données et la sauvegarde de ceux ci

### Internet

Internet est un ensemble de réseaux WAN permettenat d'inetrconnècter une grande partie de la planète. Internet n'est pas détenu par une personne mais chacun des réseau y perticipe.

### Intranet & extranet

Le terme intranet fait référence a un réseau de taille réduite appartenant à une entreprise ou a une organisation.

L'extranet est un service réseau fournis par une entreprise ou une organisation pour permettre d'ineteragir avec elle de l'exterieur de son réseau LAN ou MAN.

### Acces a internet

L'acces a internet peut s'éfféctuer par plusieurs supports : 

* **DSL** On utilise le réseau téléphonique avec la téchnologie DSL pour transmettre les données
* **Câble** On se connècte directement au réseau par un cable spécifique
* **Cellulaire** On utilise un signal sans fil téléphonque pour communiquer sur le réseau
* **Satellite** On se connècte au réseau par l'intermédière d'un satellite, plus utile dans les régions reculées
* **Ligne commutée** Une connexion à faible débit 

## Archithecture de réseau

Les réseaux permettant aujourd'hui de relier tout les types de média qu'ils soient déstinés a la diffusion, au téléphone ou a la transmission de données informatiques doivent être :

* Tolérents aux pannes : Le réseau doit toujours etre disponible malgré la panne d'un élément de celui ci
* Évolutifs : Permettant de s'agrandir rapidement pour acceuillir de nouveaux utilisateurs
* Qualitatifs : Permettant d'optimiser les transferts pour obtenir un débit le plus fort possible
* Sécurisés : Permettant de conserver la confidentialité, l'intégrité et la disponibilité des échanges

## Expention des usages

Aujourd'hui, on remarque une augmentation des usages d'internet au quotidien sur de nombreux nouveaux usages : 

* **BYOD (bring your own device)** On laisse la possibilité à l'utilisateur d'utiliser le périphérique final qu'il désire pour se connècter au réseau
* **Collaboration en ligne**
* **Communication vidéo**
* **Cloud computing** Permettant de stocker une masse de données sur internet sans avoir besoin de mobiliser sa propre équipe ou ses propres équipements

On utilise aussi de nouveau moyens de connècter les appreils finaux : 

* **Courant porteur** Les cables domestiques d'alimentation sont utilisés pour transmettre des données
* **Heut débit sans fil** Utilisant la téchnologie céllulaire

## Sécurité

La sécurité d'un réseau est primordiale et on doit mettre en place des systèmes permettant d'mepecher toutes les menaces exterieurs :

* **Virus, vers et cheval de troie** Des logiciels executant du code malveillant sur le périphérique utilisateur
* **Spyware ou Adwares** Des logiciels qui collèctent des données sur le système utilisateur
* **Zero day** Attaques le jour de la détèction de la vulnérabilité
* **Attaque pirate** Attaques éfféctuée par une personne ayant de solides dconaissances du réseau
* **Vol de données**
* **Usurpation d'identitée**

Il n'existe pas de solution maitraisse permettant de sécuriser un réseau mais on peut mettre en place un ensemble de solutions :

* Installer des antivirus et anti-logiciels éspions
* Installer un par-feu visant a filtrer les données qui entrent et sortent du réseau
* Préciser les acces de chaque personne aux ressource du réseau
* Des réseaux privés virtuels permettant un acces sécurisé hors du réseau LAN
