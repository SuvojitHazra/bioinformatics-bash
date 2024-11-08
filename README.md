# bioinformatics-bash
Introductory Bash scripts for Bioinformatics

Q1. How to write each line of a text file into a new file and give it a name that corresponds to its content?

awk '{ fname=$1 ".txt"; print > fname; close(fname) }' filename.txt

Q2. How to remove the last of a large text file using bash without opening it in a text editor?

tail -n 1 filename.txt | wc -c | xargs -I {} truncate filename.txt -s -{}


