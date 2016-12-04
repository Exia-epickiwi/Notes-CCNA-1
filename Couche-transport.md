# Chapitre 9 : Couche transport

La couche transport est chargée de l'etablissement d'une session de communication entre les applications. La couche transport a pour but de suivre les echanges des applications sur le réseau, de segmenter les données a envoyer pour correspondre au protocole de la couche internet mais aussi d'identifier les applications pouvant envoyer et recevoir des données en attribuant un numero de port a chacune d'elles.

A l'aide des en-tetes attribués a chaque segment, la couche transport peut reconstituer les données reçus dans le bon ordre malgré une multiplexion du siganl permettant de partager la bande passante.

Il existe deux types de protocoles utilisés sur la couche transport et présents dans la suite de protocoles TCP/IP

**TCP** est un protocol fiable car il trace chacun des paquets transmis par un système d'accusé de récéption. Il numérote aussi les segments permettant la reconstitution dans l'ordre des données mais aussi une retransmission des données manquantes. Ce protocol est plus lent dans la transmission mais permet une fiabilité des données dans des domaines ou la qualité de ceux ci est importante comme les bases de données, la navigation web ou l'envoie d'emails.

**UDP** est un protocol utilisant un système dit "au mieu" c'est a dire non fiable. Ainsi on envoie les données et aucun accusé de recéption n'est demandé permettant de réduire la charge requise pour transmettre des données mais avec l'incertitude sur la qualité des données reçus. Ce protocole est utilisé dans des domaines ou la rapidité de récéption est plus importante que la qualité des données reçus comme un flux video ou audio en continue.

## TCP

Le protocole TCP a pour objectiof d'etablire une connexion permettant de verifier la connectivité entre l'hote de depart et d'arrivée, de garantire la livraison par une acheminement fieble (accusé de reception), de livrer les données dans le bon ordre et enfin de controler le flux de donnés pour qu'il corresponde aux exigences du support de transmission.

