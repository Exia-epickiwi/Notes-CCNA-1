# Chapitre 10 : Couche application

**La couche application** comprends tout les protocoles permettant de faire communiquer l'application en contact avec l'utilisateur et le réseau. On y voie des protocoles comme HTTP, FTP, SSH, etc.

**La couche présentation** a pour but de présenter les données dans une forme compréensible par l'autre hote. On y retrouver des formats de compressioçns et d'encodage de video, d'audio, d'image, etc.

**La couche session** a pour but de maintenir un dialogue entre les applications sources et distantes.

La couche application se représente le plus souvent comme un système client-serveur. Dans ce système, le client demande des sinformations au serveur qui répond par un ou plusieurs flux de données.

La couche application peut aussi utiliser un système peer-to-peer permettant un echange décentralisé entre les hotes. Ce système est notemment utilisé dans le protocole gNutella ou Bittorent permettant la prtage de fichiers.

Le protocole HTTP permet de recupèrer un page Web sur le WorldWideWeb codé en HTML permettant a chaque navigateur de l'interprèter. Ce protocole bien qu'effichace n'est pas tres sécurisé et le protocole HTTPS est mis en place pour garantire cette sécurité par le chiffrement des flux.