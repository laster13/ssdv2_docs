<br /><img src="https://user-images.githubusercontent.com/64525827/107496602-ceddbb80-6b91-11eb-9a05-ac311eedf150.png" width="450">
<br />

>[!note]+
> You need a NON-root user, who has sudo rights.

[![Discord: https://discord.gg/EyV5f5ZyYF](https://img.shields.io/badge/Discord-gray.svg?style=for-the-badge)](https://discordapp. com/invite/kkwEvV6dfj)

### The SSD script allows the installation of a complete seedbox with Docker

To begin the installation, you must first follow the following steps:
* [A remote server](https://github.com/projetssd/ssdv2/wiki/Serveur)
* [A domain name](https://github.com/projetssd/ssdv2/wiki/Nom-de-domaine)
* [Cloudflare DNS](https://github.com/projetssd/ssdv2/wiki/Cloudflare)
* [Google Drive API creation](https://github.com/projetssd/ssdv2/wiki/Cr%C3%A9ation-API-Google)

Once the prerequisites have been validated, you can follow the guide:

On Debian, you have to start by installing sudo
```
apt-get update
apt install -y sudo
```

If you only have root:
```
adduser seed # change "seed" to the user you want, and answer the questions
usermod -aG sudo seed # change "seed" to the user you want
```
Once all this is done, log out of your root session, and reconnect with the user that has just been created

For the following, we assume that the directory which will receive the sources is /home/${USER}/seedbox-compose, but this directory can be changed

Afterwards
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
You will get this message:
```
IMPORTANT !
==================================================== =
Your user was not in the docker group
It has been added, but you must disconnect/reconnect for the rest of the process to work
==================================================== =
```
So disconnect then reconnect and continue with the same command
```
cd /home/${USER}/seedbox-compose && ./seedbox.sh
```

[![Discord: https://discordapp.com/invite/kkwEvV6dfj](https://img.shields.io/badge/Discord-gray.svg?style=for-the-badge)](https:// discordapp.com/invite/kkwEvV6dfj)


#### Once the prerequisites have been validated, you can follow the guide:  
* [Step by step installation](https://github.com/projetssd/ssdv2/wiki/pas-%C3%A0-pas)

> The installation can also be done on a home server, however this wiki will only talk about cloud installation on a remote server.

##JetBrains
thanks to [<img src="./images/jetbrains-training-partner.svg" alt="JetBrains" width="32"> JetBrains](http://www.jetbrains.com/) for open source licenses which allow us to work on this project.

* [<img src="./images/icon-phpstorm.svg" alt="PhpStorm" width="32"> PhpStorm](http://www.jetbrains.com/phpstorm/)
* [<img src="./images/icon-webstorm.svg" alt="WebStorm" width="32"> WebStorm](http://www.jetbrains.com/webstorm/)
* [<img src="./images/icon-pycharm.svg" alt="Pycharm" width="32"> Pycharm](http://www.jetbrains.com/pycharm/)

> This script is provided for experimental purposes only, downloading copyrighted works is illegal.
Please comply with the legislation in force in your respective countries by carrying out your tests on royalty-free files.