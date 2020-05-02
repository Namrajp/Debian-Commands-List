# Debian-Commands-List
## User commands Basics

 [To Download google Chrome](http://www.google.com/chrome)
 **Type wget** http://www.google.com/chrome

<u>To Search downloaded files</u> 
`$ apt-cache search google-chrome`

#### TO install the Debian Package
  $ sudo dpkg -i google-chrome-stable_current_amd64.deb 
 List Processes using ps and grep to select process related to apt command
 `ps aux | grep -i apt` 
 
 * To kill multiple processes (using pIds)causing Lock or error and flag -9 to force kill
 `+sudo kill -9 5313 5314 20070`
 
 * $I can type <b> `lsblk` </b> to list disk devices for viewing disk usages and disk free space.
  + `cfdisk` to format disk or make disk partitions

#### Enable Firewall
`namraj@linux:~$sudo ufw enable`
 or
`$ sudo ufw status verbose`
`$ sudo ufw status`
`Status: active`

#### Make Ubuntu Hibernate Instead Of Sleep

hit `Alt+F2`, type in `gconf-editor` and hit Enter.

### Install tree
`namraj@linux:~/Documents/sites/node-test$ sudo apt install tree`
#### Install npm package left-pad
`namraj@linux:~/Documents/sites/node-test$ npm install left-pad --save`


#### Download in step 2 and in 3 add sublime repo to my system..:Once the repository is enabled, update apt sources

sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"

sudo apt update
sudo apt install sublime-text

enjoy sublime text 
next

https://linuxize.com/post/how-to-install-wordpress-with-apache-on-ubuntu-18-04/

  
   

