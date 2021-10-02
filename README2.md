# 关于

## 网站

Website is op basis van [Docute](https://github.com/QuintenMadari/docute) (vue). Wordt niet langer onderhouden, dus geforkt.
Met behulp van een git [submodule](https://github.com/QuintenMadari/yiqizuozuoye) in de site [repo](https://github.com/QuintenMadari/zuoye) kunnen we door te committen en te pushen ons huiswerk uploaden. Site wordt up to date gehouden aan de hand van een python script en een deploy script op de server die elke 15 minuten cront.  

## cron

```
crontab -e
m h    dom mon dow    command
*/15 * * * * deployzuoye.sh
```
## letsencrypt

Zorg er wel voor dat apache2 sites available klopt.

```
sudo apt install certbot
sudo apt install python3-certbot-apache
sudo certbot run -a webroot -i apache -w /var/www/html -d qsrm.win -d www.qsrm.w>
```
