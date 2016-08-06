#Readme#

Box vagrant basée sur la box bento : [bento/debian-8.5-i386](http://https://atlas.hashicorp.com/bento/boxes/debian-8.5-i386)
##Spécification de la box ##
Debian 8 (Jessie)
Apacche 2.4 avec MPM Worker
PHP5-FPM 5.6
MySQL 5.5.50

## Outils installés dans la box ##
Webmin 
- url : https://localhost:10000/
- compte : vagrant/vagrant

PhpMyAdmin :
- url : http://localhost/pma
- compte : root/admBD

##Configuration de la box##
Ajout des dépots dotdeb https://www.dotdeb.org/

###Configuration PHP###
display_errors on
ServerTokens Full

###Configuration Apache###
Module Rewrite activé

###Configuration MySQL###
Compte root : root/admBD
Ajout d'une base de données prête à l'emploi : testdb avec utilisateur test_user/test_pwd

##Utilisation de la box##
Placer le fichier .box du package dans le dossier de stockage des box.

Dans le dossier de travail :
`vagrant init`

Puis remplacer le fichier Vagrantfile généré par celui du package.
Adapter la directive config.vm.box_url par le chemin vers le fichier .box téléchargé.

Lancement de la VM 
`vagrant up`