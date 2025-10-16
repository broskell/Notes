Linux Commands Cheat Sheet
A concise, beginner-friendly reference for common Linux commands, with corrected examples and quick explanations.
Contents
Navigation
Files and directories
Viewing and paging
Search and find
Links
Permissions and ownership
System info and help
Text processing
Regex quick guide
Safety tips
Navigation
pwd — print working directory
cd — change directory
cd or cd ~ — go to home directory
cd - — switch to previous directory
cd .. — up one level
cd ../.. — up two levels
ls — list files
ls -a — include hidden files
ls -l — long listing with permissions and sizes
ls -la — long listing including hidden files
ls -ltr — sort by time, newest last
Files and directories
mkdir name — create directory
touch file — create empty file or update its timestamp
touch -c file — do not create if missing
cat file — print file contents
cat > file.txt — write from stdin, overwrites file
cat >> file.txt — append from stdin
cp SRC DEST — copy file
cp -r SRC_DIR DEST_DIR — copy directory recursively
mv SRC DEST — move or rename
rm file — remove file
rm -f file — force remove, no prompt
rm -r dir — remove directory recursively
rmdir dir — remove empty directory
Viewing and paging
less file — pager for viewing content
head file — first 10 lines
head -n 25 file
tail file — last 10 lines
tail -n 50 file
tail -f file — follow appended output
Search and find
which cmd — path to an executable
locate name — fast filename lookup using a database
find PATH -name "pattern" — search by name in directory tree
Examples:
find . -type f -name "*.txt"
find /var/log -type f -mtime -1
grep "pattern" file — print lines matching a pattern
grep -i case-insensitive
grep -r recursive
grep -n show line numbers
Tip: the command is grep, not “gref”
Links
ln SRC LINK — hard link
ln -s SRC LINK — symbolic (soft) link
Permissions and ownership
chmod MODE file — change permissions
Symbolic: chmod u+rwx,g+rx,o-r file
Octal: chmod 755 script.sh
chown USER file — change owner
chown USER:GROUP file — change owner and group
chgrp GROUP file — change group
System info and help
man cmd — manual for a command
cmd --help — short help for many commands
wc file — line, word, byte counts
wc -l, wc -w, wc -c
Text processing
echo "text" — print a line of text
paste file1 file2 — merge lines side-by-side
cut -d',' -f1,3 file.csv — select fields
diff fileA fileB — line-by-line difference
Common pipelines:
cat file | grep pattern | wc -l
grep -r "ERROR" logs/ | less
Regex quick guide for grep/egrep
. — any single character except newline
* — zero or more of preceding
? — zero or one of preceding
+ — one or more of preceding
^ — start of line
$ — end of line
[abc] — any one of a, b, or c
[^abc] — any one character except a, b, or c
[a-z] — range
{m,n} — repetition count range
\w — word char [A-Za-z0-9_]
\d — digit
\s — whitespace
(a|b) — a or b
Escape special chars with \ when you need literal matches
Tip: use extended regex with grep -E to enable +, ?, {} without escaping.
Safety tips
Test destructive commands with echo first:
echo rm -rf "$TARGET"
Prefer interactive prompts when unsure:
rm -ri dir
Quote paths with spaces:
mv "My File.txt" "MyFile.txt"
Examples
# Create a project and navigate
mkdir -p projects/demo && cd projects/demo && pwd

# Make files and list with details
touch README.md main.py
ls -la

# Search recursively for TODOs
grep -Rni "TODO" .

# Find large logs modified in last day
find /var/log -type f -size +5M -mtime -1 -print

# Compare two configs
diff -u config.old config.new | less

# Fix permissions and ownership
chmod 755 deploy.sh
chown ubuntu:ubuntu deploy.sh

