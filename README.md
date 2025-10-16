My notes
LINUX COMMANDS 
pwd - print working directory
mkdir - make directory

diff b/w directory & file
directory is bag and file is book

cd - change direcotry
   - cd      - main directory
   - cd -    - swap
   - cd..    - one step back
   - cd../.. - two steps back
   - cd ~    - main directory
ls - listing
   - ls -a = lists hidden files
   - ls -l = lists files with principles & octal codes
   - ls -la = lits hidden files with octal codes
   - ls -ltr = lists according to time with octal codes
cat - concatenate
    - cat file.txt - creates a file
    - cat > file.txt - creates if not existed, if exists it overrides
    - cat >> file.txt - appends 
cp – Copy a file or directory to another location
man or --help – The standard unix documentation system
mv – Move or rename a file or directory
rmdir – Delete an empty directory
touch – Create a new file or update its modification time
      - touch -c - it won't create file it already exists.
rm – Delete a file or directory tree
   - rm -f
   - rm -r 
which - locate a command 
wc - print newline, word, and byte counts for each file

less – opposite of more
locate - find files by name
ln – Link one file/directory to another
find – Search for files through a directory hierarchy
chgrp – Change the group of a file or directory
chmod – Change the permissions of a file or directory
chown – Change the owner of a file or directory


echo – display line of text
cat – Concatenate files to standard output
less – Improved more-like text pager
head – Output the first parts of a file
tail - Output the last parts of a file
cut – Remove sections from each line of a file or standard input
paste - merge lines of files
diff – Compare two text files line by line


find - goes to all files 
locate - only selected files and fast
gref - global regular expression print [Print lines matching a pattern]
     - . - finds charac in a single but not new line.
     - * - finds charc which is [one or more]
     - ? - finds charac preceeding or next [0 or 1]
     - + - Matches one or more occurrences of the preceding character or group.
     - $ - Matches the end of a line or string.
     - ^ - find the words starting with it
     - [] - Matches any single character within the brackets
     - {} - range 
     - /w - words {a-z A-Z 0-9 including underscore and all}
     - /d - digits 
     - /s - spacing 
     - [a | b] - either a or b.
\ - special charc which escapes commands but not in []

