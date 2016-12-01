# Chapitre 6 : Couche réseau

## Protocole IP

La couche réseau manipule des paquets et soccupe de :

* **L'adresse des périphériques finaux** permettant de les localiser sur le réseau
* **L'encapsulation** des données du PDU de la couche précédente avec des informations comme l'adresses IP source et destination
* **Le routage** permettant de diriger les informations dans la bonne direction sur le réseau
* **La désencapsulation** d'un paquet arrivant sur la machine du réseau

Le protocol IP est un protocol sans connexion (qui n'effectue pas de connexion avec la destination avant d'envoyer le paquet), ne permet pas de suivre les paquets et donc ne permet pas de gèrer la bonne livraison de celui-ci. Et enfin est indépendant du support sur lequel il est utilisé mais adapte la taille de ses paquets en fonction de celui ci. L'en tête IP ne contiens pas beacoup d'informations a pars les adresses IP de la source et de la destination.

### En têtes IPv4

Les en-têtes d'un paquet IPv4 sont les suivants :

* **version** (4 Bits) La version de IP utilisée (ici `0100`)
* **Service différenciés** (8 Bits) Donne la priorité à certains paquets
* **Time-To-Live (TTL)** (8 Bits) Permet de limiter la durée de vie d'un paquet; des qu'un paquet est traité par un routeur, il diminue de 1
* **Protocole** (8 Bits) Le protocole utilisé par la couche précédente
* **Adresse IP source** L'adresse IP de la machine éméttrice du paquet
* **Adresse IP de destination** L'adresse IP de la machine a qui le paquet est destiné

> Exemple de protocoles :
> * *ICMP* 1
> * *TCP* 2
> * *UDP* 17

### Limites

Aujourd'hui, le protocole IPv4 fait face a plusieurs limites. Tout d'abort, les adresse IP disponibles vont venir à manquer due a l'augmentation du nombre d'appareils connectés. Les tables de routage des routeurs réseau se remplissent de plus en plus et cela provoque une augmentation des ressources nécéssaires. Pour eviter d'exposer un réseau entier, le système de NAt est mis en place et empeche d'avoir une adresse IP publique de bout en bout.

## IPv6

Pour résoudre les problèmes de l'IPv4, l'IPv6 fut crée permettent un espace d'adressage sur 128 bits au lieu de 32 qui permet de créer 340 Unidécilions d'adresses. Un traitememnt plus éfficace des paquets et l'inutilité du système de NAT due au grand nombre d'adresses IP.

Par rapport a l'IPv4, les en-têtes on été modifiés pour les simplifier. Ainsi on conserve le champ de version, le champ d'adresse source et l'adresse de destination mais on modifie les position de certains et on en supprime d'autres. Ainsi, le protocol IPv6 offre :

* Un format d'en-tête simplifié
* Davantage de données utiles
* Une archithecture réseau hiérarchique
* Une configuration automatique des adresses
* Plus besoin de NAT (Magic)

### En-têtes

* **Version** (4 bits)
* **Classe de trafic** (8 bits) Permet de donner une priorité au paquet
* **Ètiquetage de flux** (20 bits) permet de spécifier que tout les paquet qui portent la même etiquette de flux doivent etre traités de la même manière
* **Longueure des données utiles** (16 bits)
* **En-tête suivant** (8 bits) Indique le type de données trasportés par le paquet
* **Limite du nombre de fronçons** (8 bits) représente le TTL
* **Adresse source**
* **Adresse de destination**

## Routage

Pour communiquer, une machine paut envoyer des données a lui même par une adresse de bouclage; a un hote local sur le même réseau que lui ou a un hote distant au travers de la passerelle par defaut.

La passerelle par defaut est la machine permettant d'acheminer le traffic sur un réseau distant, il dispose d'une adresse IP sur les deux réseaux et permet de transmettre les donnes de l'un sur l'autre.

Chaque hote sur le réseau dispose d'un table de routage sur chacune de ses interfaces permettant de conclure si le paquet à envoyer est sur le réseau local ou non.

La table de routage d'un routeur permet d'associer un réseau a une interface. Ce réseau peut etre découvert automatiquement ou bien configuré manuellement.

Dans le cas d'un réseau local directement connècté a une interface, une ligne de cette table de routage se compose de la lettre `C` lors d'une decouverte automatique ou `L` lors d'une configuration manuelle. Suivi de l'adresse IP et du masque du réseau concerné et enfin l'interface sur laquel est associée ce réseau.

Une ligne de routage d'un réseau distant se compose des élément suivants dans l'ordre :

* **Origine de la route** La méthode utilisée pour découvrir le réseau; cela peut etre `S` pour une route statique, `D` pour Enhaced Interior Gateway Routing Protocol ou un `O` pour Open Shortest Path First
* **Réseau de destination** le réseau vers lequel les paquets peuvent etre routés
* **Distance administrative** Un chiffre permettant de vérifier la fiabilité d'une route, plus le chiffre est faible, plus la route est fiable
* **M étrique** Une valeur permettant de donner un valeur pour atteindre le réseau, une valeur faible sera préfèrée
* **Tronçon suivant** L'adresse vers le réseau local au routeur permettant d'atteindre le réseau spécifié
* **Horodatage de la route** permettant de spécifier a quel moment la route fut maintenu pour la derniere fois
* **Interface de sortie** Interface vers laquelle envoyer le paquet pour aller dans cette route

## Routeurs

Les routeurs ne sont que des ordinateurs composés d'un système d'exploitation (IOS), d'un processeur, de mémoire vive et de mémoire morte.

* **La mémoire vive** permet de stocker ponctuellement des informations rapidement
* **La mémoire morte** Contiens les données ne pouvant etre modifiés (sauf par cisco bien sur)
* **La mémoire vive non volatile** utilisée comme stockage permanent du fichier de configuration `startup-config`
* **Mémoire flash** Mémoire non volatile contenant le système et les journaux de log
* **Module d'integration avancée** permettant de décharger le processeur des actions importantes en temps comme la cryptographie

Lors du démarrage, le système compris dans la mémoire flash est chargé dans la memoire vive ainsi que la fichier de configuration global. Le démarrage s'éfféctue selon le processus suivant

1. **Execution des tests POST et chargement du programme de démarrage** un diagnostique téchnique et d'alimentation du routeur suivi du chargement du système dans la RAM
2. **Chargement de IOS**
3. **Localisation et chargement du fichier de configuration**

> Zeu good fact : Pour voir la version de cisco IOS en cours il faut taper la commande `show version`

## Configuration d'un routeur

Nous ne reviendrons pas ici sur la configuration de base du périphérique car elle a deja été vue dans le [chapitre 2](./Configuration-d'un-système-d'exploitation-réseau.md).

La configuration d'une interface passe par plusieurs commandes executés depuis la configuration globale.

```
# On entre dans le mode de configuration d'interfaces
interface gigabitethernet 0/0
# On configure le réseau de l'interface
ip address 192.168.10.1 255.255.255.0
# On configure la passerelle par défaut
ip default-gateway 192.168.10.50
# On donne une déscription pour l'interface
description Link to LAN-10
# On (re)démarre l'interface
no shutdown
```

On peut alors vérifier sa configuration avec l'une des commandes

* `show ip interface brief` Affiche un apperçu des interfaces
* `show ip route` Affiche la table de routage
* `show interfaces` Affiche les statistiques des interfaces
* `show ip interface` Affiche les statistiques IPv4 des interfaces


