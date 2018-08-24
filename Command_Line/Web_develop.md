check to ensure the server is up:
ps -aef | grep httpd

sudo apachectl start
sudo apachectl stop
sudo apachectl -k restart
The -k will force a restart immediately rather than asking politely to restart when apache is good and ready

open -e /usr/local/etc/httpd/httpd.conf








PHP
/usr/local/etc/php/5.6/php.ini
/usr/local/etc/php/7.0/php.ini
/usr/local/etc/php/7.1/php.ini
/usr/local/etc/php/7.2/php.inih