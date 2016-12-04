# Chapitre 9 : Couche transport

La couche transport est chargée de l'etablissement d'une session de communication entre les applications. La couche transport a pour but de suivre les echanges des applications sur le réseau, de segmenter les données a envoyer pour correspondre au protocole de la couche internet mais aussi d'identifier les applications pouvant envoyer et recevoir des données en attribuant un numero de port a chacune d'elles.

A l'aide des en-tetes attribués a chaque segment, la couche transport peut reconstituer les données reçus dans le bon ordre malgré une multiplexion du siganl permettant de partager la bande passante.

Il existe deux types de protocoles utilisés sur la couche transport et présents dans la suite de protocoles TCP/IP

**TCP** est un protocol fiable car il trace chacun des paquets transmis par un système d'accusé de récéption. Il numérote aussi les segments permettant la reconstitution dans l'ordre des données mais aussi une retransmission des données manquantes. Ce protocol est plus lent dans la transmission mais permet une fiabilité des données dans des domaines ou la qualité de ceux ci est importante comme les bases de données, la navigation web ou l'envoie d'emails.

**UDP** est un protocol utilisant un système dit "au mieu" c'est a dire non fiable. Ainsi on envoie les données et aucun accusé de recéption n'est demandé permettant de réduire la charge requise pour transmettre des données mais avec l'incertitude sur la qualité des données reçus. Ce protocole est utilisé dans des domaines ou la rapidité de récéption est plus importante que la qualité des données reçus comme un flux video ou audio en continue.

## Ports

La gestion des ports permettent a plusieurs applications de communiquer sur le même système. Pour se faire on attribue un port a chaque application pour cmmuniquer. Un port **source** et un port **destination**. Avec l'adresse IP et le port, on a toutes les informations pour se faire communiquer deux applications précises sur deux systèmes distants. Il existe différents types de numerots de ports :

* **Ports réservés (0-1023)** permettant a des applications standards de communquer
* **Port enregistrés (1024-49151)** enregistrablme aupres de l'IANA par des entreprises permettant de normaliser les ports utilisés
* **Ports privés ou dynamiques (49152-65535)** ports attribués dynamiquement par un hote por permettre un conexion dans les deux sens

> Quick tip : La commande `netstat` permet d'afficher les ports utilisés sur une machine

Un même port ne peut etre utilisé par deux applications simulatément et seul les paquets demandant une connexion sur un port ouvert sont accèptés.

## TCP

Le protocole TCP a pour objectiof d'etablire une connexion permettant de verifier la connectivité entre l'hote de depart et d'arrivée, de garantire la livraison par une acheminement fieble (accusé de reception), de livrer les données dans le bon ordre et enfin de controler le flux de donnés pour qu'il corresponde aux exigences du support de transmission.

Pour arriver a cela, le protocol inclue les en-têtes suivants :

* **Port source et port destination (32Bits)** permettant de definir l'application avec laquelle communiquer
* **Numéro d'ordre (32 Bits)** permettant la réorganisation des données
* **Numéro d'accusé de reception (32 Bits)** permettant d'indiquer la reception des données
* **Longeure d'en-tête (4 bits)** La taille des ten-têtes TCP
* **Plage réservée (6 Bits)**
* **Controle (6 bits)** Indiquant l'objectif du segment
* **Taille de la fenetre (16 bits)** Le nombre de segments acceptés en même temps
* **Somme de contrôle (16 bits)** utilisé pour controler les érreurs du segment
* **Urgent (16 bits)** indique si un paquet est urgent

Pour éfféctuer une connexion, 3 etapes sont requises.

1. Le client demande une connexion au serveur (requète SYN)
2. Le srveur accuse récéption et demande uyne connexion vers le client (requète SYN et ACK)
3. Le client accusé récéption de la connexion depuis le serveur (requète ACK)

Pour fermer un connexion, on procède comme suit :

1. Le client envoie une requète de fin (requète FIN)
2. Le serveur accuse récéption et envoie un segment de fin (Requète ACK et FIN)
3. Le client accuse récéption du segment fin (Requète ACK)

Chaque connexion TCP se déroule en 3 etapes :

1. On vérifie que le périuphérique de destination est bien présent
2. On s'assure que le périphérique de destination dispose d'une apllication sur le port défini
3. On informe le périphérique de la demande de connexion

Ces connexions sont orchéstrés par l'en tête de controle pouvant prendre comme valeurs :

* **URG** Paquet urgent
* **ACK** Accusé de récéption
* **PSH** Fonction push
* **RST** Reinitialiser la connexion
* **SYN** Syncronisation des numeros de séquence
* **FIN** Abscence de données de l'expéditeur (fin de connexion)

Pour recoonstituer les données dans le bon ordre, un numéro permettant de les réordonnés est conclu lors de la connexion, ce numéro initial appelé ISN est un nombre aléatoire servant de base a toute la connexion.

Pour eviter d'accuser la récéption de toute les segments, on met en place un taille de fenetre tant la taille maximale de données que peut recevoire le serveur sans avoir besoin d'un accusé de récéption. Rien n'empeche le erveur d'accuser la récéption avant.

Le protocole TCP inclue un système de gestion de l'encombrement du réseau permettant d'optimiser les transferts. Ainsi le client peut réduire le numbre d'octets avant l'accusé de reception pour fluidifier le réseau.

> Exemples : Applications utilisant TCP
> * HTTP
> * FTP
> * SMTP
> * Telnet

## UDP

Le protocole UDP est bien plus simple car il a vocation a etre rapide et doit réduire au minimum son ajout de données ou l'envoie de segments superflux. Ainsi l'en-tête UDP ne se compose que de 8 Octets comprenant :

* **Port source et destination (32 bits)**
* **Longeure de données (16 bits)**
* **Somme de controle (16 bits)**

Le protocole UDP malgré sa simplicité reste utile et plus ou moins fiable. En effet, si aucune reponse n'est recu durant un certain temps, les paquets envoyés au depart sont réenvoyés.

Le protocole UDP ne fournis pas de sytstème permettant de réassembler les données, il sont simplement reassemblés dans l'ordre dans lequel ils sont arrivés. Dans le cadre de ce protocole les données sont séparés en **datagrammes**. Si l'ordre est important pour l'application, c'est a elle de les reordonner.

> Exmples : Applications utilisant UDP
> * DHCP
> * DNS
> * SNMP
> * TFTP
> * VoIP
> * Television sur IP