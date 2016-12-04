# Chapitre 8 : Segmentation des réseaux IP en sous-réseaux

Les sous réseaux sont des ensembles de materiels commnectes pouvant s'envoyer des paquets de diffusion. Un routeur permet de faire la liaison entre deux réseaux mais ne transmet pas les paquets de diffusion. Ainsi, un routeur permet de créer un sous réseau.

Un sous réseau est utile pour réduire le traffic sur un même réseau et ainsi augmenter ses performances. On peut en créer suivant des scémats particuler comme les etages d'un batiment, les entités d'une entreprise ou autre.

Pour créer un sous-réseau, on ségment l'adresse IP pour ajouter le numéro du sous-réseau a celui de du précédent.

En entreprise, la creation de sous réseau est interessant et requière de bien réfléchir a la structure général avant toute installation. Il faut penser a fournir un controle d'acces, eviter les doublons d'adresse et surveiller la sécurité et les performances.

De plus chacun des sous réseaux doit prévoire une adresse pour donner un acces a tout appreil se connectant, un acces distant au serveur sur le réseau, une passerelle permettant d'atteindre les réseaux de couche superieur.

Dans le cas d'une adresse IPv6, la creation de sous réseaux s'effectue en modifiant une partie de l'identifiant réseau.