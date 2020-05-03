# Linux commands for local server setup and configurations
## In this guide 
* How to install google chrome and opera browser
* How to install a debian package
* How to enable firewall
* Make Ubuntu Hibernate Instead Of Sleep
* How to install a npm package left-pad
* How to install apache
* How to instal PHP
* How to instal Wordpress
* Setting up virtual hosts

 [To Download google Chrome](http://www.google.com/chrome)
 **Type wget** http://www.google.com/chrome

<u>To Search downloaded files</u> 
`$ apt-cache search google-chrome`

##### Opera setup
`wget -qO- https://deb.opera.com/archive.key | sudo apt-key a
sudo add-apt-repository "deb [arch=i386,amd64] https://deb.opera.com/opera-stable/ stable non-free" `

---

#### TO install the Debian Package
  `$ sudo dpkg -i google-chrome-stable_current_amd64.deb` 
 List Processes using ps and grep to select process related to apt command
 `ps aux | grep -i apt` 
 
 * To kill multiple processes (using pIds)causing Lock or error and flag -9 to force kill
 `+sudo kill -9 5313 5314 20070`
 
 * $I can type <b> `lsblk` </b> to list disk devices for viewing disk usages and disk free space.
  + `cfdisk` to format disk or make disk partitions
---
#### Enable Firewall
`namraj@linux:~$sudo ufw enable`
 or
`$ sudo ufw status verbose`
`$ sudo ufw status`
`Status: active`

---

#### Make Ubuntu Hibernate Instead Of Sleep

hit `Alt+F2`, type in `gconf-editor` and hit Enter.

### Install tree
`namraj@linux:~/Documents/sites/node-test$ sudo apt install tree`
#### Install npm package left-pad
`namraj@linux:~/Documents/sites/node-test$ npm install left-pad --save`


#### Download in step 2 and in 3 add sublime repo to my system..:Once the repository is enabled, update apt sources

`sudo apt install apt-transport-https ca-certificates curl software-properties-common`
`curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`
`sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"`

`sudo apt update`
`sudo apt install sublime-text`

enjoy sublime text 
next

https://linuxize.com/post/how-to-install-wordpress-with-apache-on-ubuntu-18-04/

---
##### How to install apache

 sudo apt update
 sudo apt install apache2
sudo systemctl status apache2  # check apache service status
sudo ufw allow 'Apache Full' #If your Ubuntu server is protected by a firewall you’ll need to open HTTP (80) and HTTPS (443) ports.
`sudo ufw status`
http://localhost/ #verify

Apache Configuration File’s Structure and Best Practices
All Apache configuration files are located in the /etc/apache2 directory.
The main Apache configuration file is /etc/apache2/apache2.conf.
The ports that Apache will listen to are specified in the /etc/apache2/ports.conf.

You can set your domain document root directory to any location you want. The most common locations for webroot include:
/home/<user_name>/<site_name>
/var/www/<site_name>
/var/www/html/<site_name>
/opt/<site_name>
Conclusion
You have successfully installed Apache on your Ubuntu 18.04 server. You’re now ready to start deploying your applications and use Apache as a web or proxy server.

https://linuxize.com/post/how-to-install-apache-on-ubuntu-18-04/#install-apache
https://linuxize.com/post/secure-apache-with-let-s-encrypt-on-ubuntu-18-04/

[how-to-install-mysql-on-ubuntu](https://linuxize.com/post/how-to-install-mysql-on-ubuntu-18-04/)

Next only left to install wordpress as follow below link put your username and password on grant user and pasword mistake is 
GRANT ALL ON wordpress.* TO 'wordpressuser'@'localhost' IDENTIFIED BY 'change-with-strong-password';

GRANT ALL ON wordpress.* TO 'namraj'@'localhost' IDENTIFIED BY 'codingkode23';


[how-to-install-wordpress-with-apache-on-ubuntu-18-04](https://linuxize.com/post/how-to-install-wordpress-with-apache-on-ubuntu-18-04/)

---
##### Installing PHP

 sudo apt install php7.2 php7.2-cli php7.2-mysql php7.2-json php7.2-opcache php7.2-mbstring php7.2-xml php7.2-gd php7.2-curl

sudo systemctl restart apache2
---
##### Installing wordpress 
Create a directory to hold wordpress eg. 
`sudo mkdir -p /var/www/example.com`
`cd /tmp`
`wget https://wordpress.org/latest.tar.gz`
`tar xf latest.tar.gzsudo `
`sudo mv /tmp/wordpress/* /var/www/example.com/`
`sudo chown -R www-data: /var/www/example.com`

`sudo nano /etc/apache2/sites-available/example.com.conf`
copy ssl licence
sudo a2ensite example.com

Enabling module socache_shmcb.
Enabling module ssl.
See /usr/share/doc/apache2/README.Debian.gz on how to configure SSL and create self-signed certificates.
To activate the new configuration, you need to run:
  systemctl restart apache2
namraj@linux:~$ sudo a2enmod headers
Enabling module headers.
To activate the new configuration, you need to run:
  systemctl restart apache2
namraj@linux:~$ sudo a2enconf letsencrypt

systemctl restart apache2
`namraj@linux:~$ sudo systemctl reload apache2`
`namraj@linux:~$ sudo certbot certonly --agree-tos --email` 
`admin@example.com --webroot -w /var/lib/letsencrypt/ -d example.com -d www.example.com`

> Saving debug log to /var/log/letsencrypt/letsencrypt.log
Plugins selected: Authenticator webroot, Installer None
There seem to be problems with that address. Enter email address (used for
urgent renewal and security notices)

If you really want to skip this, you can run the client with
--register-unsafely-without-email but make sure you then backup your account key
from /etc/letsencrypt/accounts

 (Enter 'c' to cancel): 
Invalid email address: .
Enter email address (used for urgent renewal and security notices)


If you really want to skip this, you can run the client with
--register-unsafely-without-email but make sure you then backup your account key
from /etc/letsencrypt/accounts

 (Enter 'c' to cancel): actice99raj@gmail.com
---
 ##### Setting up Virtual Hosts
 
 Ubuntu Home folder in windows subsystem 
C:\Users\onesi\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc\LocalState\rootfs
cd /mnt/c to go to c dir
namraj@Namraj-4GZ7:/mnt/c/Users/onesi/Documents$

---
To install xampp with wordpress

-Install xampp with php7 open 
- Go to Control center and start apache and mysql
- Then go to localhost and verify apache running
- Next delete all files in htdocs folder and download and extract wordpress folder in htdocs
- Navigate to localhost/wordpress to setup wp , type username root database wordpress or whatever
- Set field of password to empty and localhost next. If this setup dont work then open wp-config-sample file
- Rename to wp-config and type manually db:wordpress user:root password:empty localhost save and` 
try localhost/wordpress. 

---
###$ To setup domain in vhost

# Go to folder C:\xampp_new\apache\conf\extra\httpd-vhosts open this file copy <virtualHost> block and edit like :
####<VirtualHost *:80>
    -ServerAdmin webmaster@dummy-host2.example.com
    -DocumentRoot "C:/xampp_new/htdocs/dummy-host2.example.com"
    -ServerName dummy-host2.example.com
    -ErrorLog "logs/dummy-host2.example.com-error.log"
    -CustomLog "logs/dummy-host2.example.com-access.log" common
####</VirtualHost>

<VirtualHost *:80>
   DocumentRoot "C:/xampp_new/htdocs/wordpress"
   ServerName woocommerce.test
</VirtualHost>


C:\Windows\System32\drivers\etc drag into desktop and edit  add line 
127.0.0.1 woocommerce.test and drag back---due to permissions to edit there itself.

- lastly, go to phpmyadmin to select wordpress database and select wp-options
- change siteurl and home to http://woocommerce.test

  
   

