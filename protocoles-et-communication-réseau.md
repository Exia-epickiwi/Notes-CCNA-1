# Chapitre 3 : Protocoles et communication réseau

## Structure d'une communication

Toute communication peut être représenté par 5 elements principaux et la communication etre ordinateurs ne fait exception : 

* La source du méssage à émettre (La machine source)
* L'émétteur du signal (la carte réseau source)
* Le support de transmission (cuivre, air ou fibre optique)
* Récépteur du message (carte réseau de destination)
* Destinataire du message (machine de destination)

Pour convenablement communiquer, les machines doivent s'accorder sur une langue partagée pour communiquer. C'est cela que l'on apelle *protocole*. Il en existre un grand nombre qui sont normalisés pour permettre une communication corrècte. ce protocol définis les informations que la machine source doit fournir pour se faire comprendre par le réseau.

Pour corrèctement transmettre le message, les machines utilisent non pas un seul protocol mais une suite de protocol ajoutant chaqun d'eu de nouvelles informations permettant de transmettre le message. On apelle cette organisation la *suite de protocoles*. Ainsi le message à envoyé est encapsulé par chacun des protocoles permettant sa transmission.

### Codage

Pour les besoins de la transmission, les données qui vons etre envoyés doivent subir une transformation permettant de les rendre compatibles avec le support de trsnmission et le protocol utilisé. C'est cette opération que l'on apelle *codage*

> Exemple : Dans une conversation téléphonique, chaque son reçu est codé sous forme de bit puis envoyé au destinataire qui reconstitue le son a parti des informations reçues.

### Encapsulation

Le message brut, même codé, ne peut etre envoyé tel quel sur le réseau, il faut lui fournir d'autre informations comme le destinatire de la lettre ou l'éxpéditeur. Ces informations sont ajoutés au début ou a la fin du message à envoyé. L'encapsulation consiste alors en l'ajout d'informations au message brut en fonction des informations requises par le réseau. L'ensemble du message encapsulé est appelé *trame* et peut etre envoyé sur le réseau. Il peut y avoir plusieurs phases d'encapsulation d'un message.

### Taille

Pour réspècte le protocol utilisé pour la transmission, le message peut etre divisée en plusieurs *trames* permettant ainsi de ne pas engorger le réseau.

### Syncronisation et gestion des trames

Lorsque deux hotes envoient une trame au même moment sur le réseau, il se produit une *collision*. Pour éviter ce genre de chose, le protocol doit définir une *méthode d'acces* définissant le moment ou les hotes doivent parler et que faire en cas d'érreur.

Pour éviter d'engorger le réseau, le protocol doit aussi spécifier un système de *controle de flux* pour donnér un chance à chaque hote d'envoyer des données sur le réseau.

Enfin, le protocol doit aussi définir un *délai d'attente*, qui dépassé, autorisera l'hote émétteur sans réponse de considèrer qu'aucune réponse n'à été donnée.

### Méthode d'envoie

L'envoie d'une trame peut s'éfféctuer de 3 façon différentes :

* **Monodiffusion** On envoie la trame a un seul hote
* **Multidiffusion** On envoie la trame a un groupe d'hotes
* **Diffusion** On envoie la trame a tout les hotes du réseau

Chacune des trames peut demander ou non un accusé de récéption.

## Protocol réseau

Les protocols qui régissent les réseaux sont des protocoles définis, précis et accèptés par toutes les machines qui l'utilisent. Il existe de nombreux protocoles et ces protocols sont organisés en *suites de protocols* permettant une bonne communication.

Un protocol peut etre :

* **Ouvert** Il est alors normalisé par un organisme de normalisation et peut etre utilisé partout et par tous
* **Propriétaire** Il est alors normalisé par l'entreprise qui l'a crée et ne peut etre utilisé que par cette même entreprise.

Il existe de nombreuses suites des protocoles mais en voici quelques exemples

![Quelques piles de protocoles](img/protocoles.png)

Nous allons ici nous concentrer sur le protocole TCP/IP

À suivre :wink:

====> 3.2.2.2 <====