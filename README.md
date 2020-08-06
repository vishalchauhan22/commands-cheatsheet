# commands-cheatsheet

 - list only directories
  - ls -d /home/alice/Documents/*/
 
 - iterate over a file line by line nand execute a command
  - while read line; do git --git-dir=$line/.git remote -v; done < dirrr
  - sleep 2; echo ""; done < file.ext
  
 - Delete/move a particular past day file
  - find ./ -type f -mtime 27 -exec mv {} /var/log/apps/baks-29052019 \;
  - find ./ -type f -mtime 36 -exec ls -l {} \; | wc -l


 - AWK
  - cat test.csv |  awk '{split($0,a,","); print a[3],a[2],a[1]}'
  
Brightness
 - xrandr --output VGA-1 --brightness 0.7


NODE_MODULES
 - tar -cvzf op.tar.gz -exclude=\*/node_modules applications/
