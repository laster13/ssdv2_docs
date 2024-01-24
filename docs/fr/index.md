[![Discord chat](https://img.shields.io/discord/533736783414820864?style=for-the-badge&color=4051B5&logo=discord){ .off-glb }](https://discord.gg/qbfdKVYB){:target="_blank" rel="noopener noreferrer"}

<br /><img src="https://user-images.githubusercontent.com/64525827/107496602-ceddbb80-6b91-11eb-9a05-ac311eedf150.png" width="450">
<br />

>[!note]+
> Il faut un user NON root, qui ait les droits de faire du sudo.

### Le script SSD permet l'installation d'une seedbox complète avec Docker

Pour se lancer dans l’installation, il faut au préalable suivre les étapes suivantes:
* [[Installation/serveur.md|Serveur]]
* [[Installation/domaine.md|domaine]]
* [[Installation/cloudflare.md|Cloudflare]]

Une fois les pré-requis validés pous pouvez suivre le guide :

Sur debian, il faut commencer par installer sudo
``` 
apt-get update
apt install -y sudo
```

Si vous n'avez que root :
``` 
adduser seed # changez "seed" par le user que vous voulez, et répondez aux questions
usermod -aG sudo seed # changez "seed" par le user que vous voulez
```
Une fois que tout ça est fait, déconnectez vous de votre session root, et reconnectez vous avec le user qui vient d'être créé

Pour la suite, on suppose que le répertoire qui va recevoir les sources est /home/${USER}/seedbox-compose, mais ce répertoire peut être changé

Ensuite
```
sudo apt-get update && sudo apt upgrade -y
```
```
sudo apt install -y git
```
```
sudo git clone https://github.com/projetssd/ssdv2.git /home/${USER}/seedbox-compose
```
```
sudo chown -R ${USER}: /home/${USER}/seedbox-compose
```
```
cd /home/${USER}/seedbox-compose && ./seedbox.sh
```
Vous aurez ce message : 
```
IMPORTANT !
===================================================
Votre utilisateur n'était pas dans le groupe docker
Il a été ajouté, mais vous devez vous déconnecter/reconnecter pour que la suite du process puisse fonctionner
===================================================
```
Alors déconnexion puis Reconnexion et on continue avec la même commande
```
cd /home/${USER}/seedbox-compose && ./seedbox.sh
```

[![Discord chat](https://img.shields.io/discord/533736783414820864?style=for-the-badge&color=4051B5&logo=discord){ .off-glb }](https://discord.gg/qbfdKVYB){:target="_blank" rel="noopener noreferrer"}

#### Une fois les pré requis validé pous pouvez suivre le guide :  
* [Pas à pas d'installation](https://github.com/projetssd/ssdv2/wiki/pas-%C3%A0-pas)

> L'installation peut également ce faire sur un home serveur, cependant ce wiki ne parlera que de l'installation cloud sur serveur distant.

## JetBrains
merci à  [<img src="./images/jetbrains-training-partner.svg" alt="JetBrains" width="32"> JetBrains](http://www.jetbrains.com/) pour les licences open source qui nous permettent de travailler sur ce projet.

* [<img src="./images/icon-phpstorm.svg" alt="PhpStorm" width="32"> PhpStorm](http://www.jetbrains.com/phpstorm/)
* [<img src="./images/icon-webstorm.svg" alt="WebStorm" width="32"> WebStorm](http://www.jetbrains.com/webstorm/)
* [<img src="./images/icon-pycharm.svg" alt="Pycharm" width="32"> Pycharm](http://www.jetbrains.com/pycharm/)

> Ce script est proposé à des fins d'expérimentation uniquement, le téléchargement d’oeuvre copyrightées est illégal.
Merci de vous conformer à la législation en vigueur en fonction de vos pays respectifs en faisant vos tests sur des fichiers libres de droits
