---
id: c8f821a5-747b-4d9c-baeb-d4d47e79a722
title: Cli
desc: ''
updated: 1608455694168
created: 1604563984600
stub: false
---

## [Unix Commands training](https://www.freecodecamp.org/news/the-linux-commands-handbook/)

## Unix Command Cheatsheet

<details><summary>
Cannot run a command| "Permission denied" Message?
</summary>

ex.
```
chmod u+x ~/Desktop/nand2tetris/tools/*.sh
```
</details>



du -s * | sort -nr > $HOME/Desktop/user_space_report.txt

[Mac OS X Command Line (Terminal)](https://ss64.com/osx/) or using command:
```
> compgen -c
```

Best command to search:
```
> ag
or use:
> man ag // to see all possible uses
```

Other command to find soemthing:
```
> find PATH_TO_SEARCH OPTIONS_TO_USE PATTERN_TO_SEARCH_FOR
ex.
search a filename: find . -name readme.md
or a path: -path \*session\* 
```
Possibles :flags: flags I can use:
-type f
-or
-not
-mtime -\<num if days> -> ex: -mtime -2
-size -> ex. -size +200k
-print -delete

Another one for search (old school):
```
grep -> ex. grep <text to search> <file to search>
Flags:
-c // count the number of occurences
-n
```

Process running on the conputer:
```
ps 
ps u (flag)
ps -e 
ps -U root (process by user)
ps -L (all possible columns)
ps -m -O %mem -u root (to sort processes by their memory usage)
ps -r -O %cpu -u root (to sort processes by their CPU usage)

```
To stop a process
```
kill
```

search and replace
```
sed "s/[aeiou]/*" text.md (just on first occurrence)
sed "s/[aeiou]/*/g" text.md (on all occurrences)
sed "s/[aeiou]/*/2" text.md (-n term)
sed "s/[aeiou]/*/i" text.md (case insensitive)
```
to zip a file
```
if I'm already in the folder I want the file(es) to be compressed
>zip -r name.zip .
or
>zip -r archive_name.zip folder_to_compress
```
create an [archive](http://conqueringthecommandline.com/book/tar)
```
tar ...
archive e zip
tar -cf ar.tar activerecord/
```
calendar:
```
cal
cal -y
cal 1979
cal 4 1979
```
concatenate files
```
cat file1.md file2.md
```

list the tree of a Dir
```
tree
tree -d (Dir only)
tree -d Desktop/ tree of a specific Dir
```

Count words in a file
```
wc filename // count lines|words|
wc -w filename // count only words
wc -l filename // count only lines
```

Find all words in a file?
```
ag <word to search> | wc -l
```

from 6:30 top prices