# commands-cheatsheet

 - list only directories
  - ls -d /home/alice/Documents/*/
 
 - iterate over a file line by line nand execute a command
  - while read line; do git --git-dir=$line/.git remote -v; done < dirrr
  
 - Delete/move a particular past day file
  - find ./ -type f -mtime 27 -exec mv {} /var/log/apps/baks-29052019 \;
