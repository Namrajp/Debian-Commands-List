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
   * Ordered lists
   + pluses
1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses   
   

