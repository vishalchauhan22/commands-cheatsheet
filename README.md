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
  - cat subdomains | awk '/Host:/ {print$3}'
  
Brightness
 - xrandr --output VGA-1 --brightness 0.7


NODE_MODULES
 - tar -cvzf op.tar.gz -exclude=\*/node_modules applications/

File count of dates of month
```
count=1
while [ $count -lt 30 ]
do
  X=$(ls -ltrh | grep "May $count" | wc -l)
  echo "May $count >> $X"
  count=`expr $count + 1`
done
```

MEMORY

`free | awk '/Mem/{printf("RAM Usage: %.0f\n"), $3/$2*100}'| awk '{print $3}'`

`ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head -5`
