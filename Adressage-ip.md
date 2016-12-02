# Chapitre 7 : Adressage IP

## IPv4

Pour éfféctuer la conversion, il faut commencer par comprendre la notation pondérée

====>7.1<====

##IPv6

Une adresse IPv6 est longue de 128 Bits et est représentée comme une suite d'enesembles de 4 signes hexadécimaux appelés segments. Pour réduire cette adresse on peut : 

* **Omettre les 0 au debut des degments** ainsi chaque segment est réduit. Cette regle ne s'applique pas aux zéros de fin de segment, ainsi, il y a toujours au moins un signe sur un segments
* **On peut omettre** un seul fois dans une adresse **une séquence complète** de 0 par les `::` ainsi si 3 segments de 0 complets se suivent, on peut les remplacer par `::`.

Les adresses IPv6 permettent la mise en place d'un monodiffusion mais aussi d'une multidiffusion pouvant etre utilisée pour la diffusion. par l'utilisation de plusieurs types d'adresses

* **Monodiffusion globale** Une adresse IP unique au niveau mondial permettant de communiquer avec une autre machine quelque soit son réseau. Une adresse de diffusion globale, se compose d'un préfixe de routage global attribué par le FAI, d'un identifiant de sous réseau le positionnant dans les sous réseaux d'une entreprise par exemple et enfin un identifiatn d'interface équivalent a la partie hote d'une adresse IPv4
* **Link-Local (FE80::/10)** Une adresse IP utilisable uniquement dans un réseau local et ne pouvant être utilisée hors de celui ci. Les adresses de ce réseau sont définies sur une plage `FE80::/10`
* **Bouclage (::1/128)** Une adresse IP permettant de contacter sa propre machine
* **local unique** Une plage d'adresse réservée pour le local permettant une communication dans un même réseau local