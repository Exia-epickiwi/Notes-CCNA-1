# Chapitre 9 : Couche transport

La couche transport est chargée de l'etablissement d'une session de communication entre les applications. La couche transport a pour but de suivre les echanges des applications sur le réseau, de segmenter les données a envoyer pour correspondre au protocole de la couche internet mais aussi d'identifier les applications pouvant envoyer et recevoir des données en attribuant un numero de port a chacune d'elles.

A l'aide des en-tetes attribués a chaque segment, la couche transport peut reconstituer les données reçus dans le bon ordre malgré une multiplexion du siganl permettant de partager la bande passante.

Il existe deux types de protocoles utilisés sur la couche transport et présents dans la suite de protocoles TCP/IP

**TCP** est un protocol fiable car il trace chacun des paquets transmis par un système d'accusé de récéption. Il numérote aussi les segments permettant la reconstitution dans l'ordre des données mais aussi une retransmission des données manquantes.