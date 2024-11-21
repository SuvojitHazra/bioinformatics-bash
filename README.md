# bioinformatics-bash
Introductory Bash scripts for Bioinformatics

Q1. How to write each line of a text file into a new file and give it a name that corresponds to its content?

awk '{ fname=$1 ".txt"; print > fname; close(fname) }' filename.txt

Q2. How to remove the last of a large text file using bash without opening it in a text editor?

tail -n 1 filename.txt | wc -c | xargs -I {} truncate filename.txt -s -{}

Q3. How to tar one folder named 'data' ?

tar -cf - data | gzip > data.tgz

Q4. How to tar multiple sub-folders inside a folder 'dir' and remove the sub-folders after tarring?

for dir in */; do tar -czvf "${dir%/}".tgz "$dir"; done; rm -r */;

Q5. How to untar multiple tarred files (.tgz or .gz) in a folder ?

for f in *.tgz; do tar -xzvf "$f"; done <br />
for f in *.gz; do tar -xzvf "$f"; done


