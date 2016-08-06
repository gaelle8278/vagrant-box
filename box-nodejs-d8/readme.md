#Vagrant Box Node.js#

Box vagrant basée sur la box bento : [bento/debian-8.5](https://atlas.hashicorp.com/bento/boxes/debian-8.5)

##Spécification de la box ##
Debian 8.5 (Jessie)
Node.js 6.3.1
npm 3.10.3

##Configuration##
Port 8082 lié au port 8080 de la VM, peut être utilisé pour développer des applications web

Présence du dossier `/home/vagrant/node.js` dans la VM synchronisé avec le dossier `node-projets` de l'environnement vagrant

##Utilisation de la box##
Placer le fichier .box du package dans le dossier de stockage des box.

Dans le dossier de travail :
`vagrant init`

Puis remplacer le fichier Vagrantfile généré par celui du package.
Adapter la directive config.vm.box_url par le chemin vers le fichier .box téléchargé.

Lancement de la VM 
`vagrant up`
