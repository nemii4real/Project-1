## Great start with project 1

`curl http://localhost:80`

`sudo apt update`

`sudo apt intall apache2`

`sudo systemctl apache2`

`sudo apt install mysql-server`

`sudo mysql_secure_installation`

`sudo mysql`

`sudo apt install php libapache2-mod-php php-mysql`


`sudo mkdir /var/www/projectlamp`


`sudo chown -R $USER:$USER /var/www/projectlamp`

`sudo vi /etc/apache2/sites-available/projectlamp.conf`


`<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>`

`sudo ls /etc/apache2/sites-available`

`sudo a2ensite projectlamp`

`sudo a2dissite 000-default`

`sudo apache2ctl configtest`

`sudo systemctl reload apache2`


`http://<Public-IP-Address>:80`

`sudo vim /etc/apache2/mods-enabled/dir.conf`

`<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>`

`sudo systemctl reload apache2`

`vim /var/www/projectlamp/index.php`

 add this `<?php phpinfo();` after installing vim

`sudo rm /var/www/projectlamp/index.php`



![apache status](./images/apache%20status.PNG)

[install openssh](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).



[openssh-key management](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement).

[markdown cheat sheet](https://www.markdownguide.org/cheat-sheet).

