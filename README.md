# Debian-Commands-List
## User commands Basics

 To Download *Google chrome* 
 **Type wget** http://www.google.com/chrome

<u>To Search downloaded files</u> 
$ apt-cache search google-chrome

#### TO install the Debian Package
  $ sudo dpkg -i google-chrome-stable_current_amd64.deb 
 List Processes using ps and grep to select process related to apt command
 ps aux | grep -i apt 
 
 *To kill multiple processes (using pIds)causing Lock or error and flag -9 to force kill
 sudo kill -9 5313 5314 20070
 
 $I can type <b> lsblk </b> to list disk devices for viewing disk usages and disk free space.
   cfdisk to format disk or make disk partitions

