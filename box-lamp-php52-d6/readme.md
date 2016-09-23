#Readme#

Box vagrant basée sur la box bento : [bento/debian-6.0.10-i386](https://atlas.hashicorp.com/bento/boxes/debian-6.0.10-i386)
##Spécification de la box ##
Debian 6 (Jessie)
Apache 2.2 avec MPM prefork
PHP5 5.2
MySQL 5.1.73

###Configuration MySQL###
Compte root : root/root

##Utilisation de la box##
Placer le fichier .box du package dans le dossier de stockage des box (D:\Virtualisation\Vagrant_custom_box\)

Dans le dossier de travail :
`vagrant init`

Puis remplacer le fichier Vagrantfile généré par celui du package.
Adapter la directive config.vm.box_url par le chemin vers le fichier .box téléchargé si nécessaire.
**Adapter config.vm.network avec l'ip à associer à la VM.**

Lancement de la VM 
`vagrant up`