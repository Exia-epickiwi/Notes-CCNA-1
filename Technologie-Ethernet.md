# Chapitre 5 : Téchnologie Ethernet

Ethernet est la téchnologie LAn la plus utilisée aujourd'hui. Elle se positionne sur la couche liaison de données et prends en charge des bandes passantes de 10, 100, 1.000, 10.000, 40.000 et 100.000 MBit/s. Cette norme définis un protocol de la couche 2 et 3 et se divise en deux sous-couches:

* **LLC** qui gère la communication entre les couches superieurs et inferieurs. Cette couche est tout a fait logicielle et indépendante du materiel. De plus elle est assez cocasse.
* **MAC** La sous-couche inferieur, elle est mise en oeuvre au niveau materiel des cartes réseau de la machine.

Ethernet fut créé en 1973 et n'a cèssé d'évoluer pour augmenter sa bande passante et devenir plus flexible.

## Sous-couche MAC

Cette sous couche à deux objectif soit encapsuler les données et controler l'acces au support.

Cette sous couche en charge de l'encapsulation gère donc 

* **La delimitaition des trames** permettant la synchronisation de l'emetteur vaec le récépteur
* **L'adressage** physique de la trame
* **Detection des érreurs**

La sous couche gère aussi l'acces au support et vérifie ainsi la disponibilité de celui ci et les éventuelles collisions.
