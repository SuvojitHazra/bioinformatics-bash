# bioinformatics-bash
Introductory Bash scripts for Bioinformatics

Q1. How can I write each line of a text file into a new file and give it a name that corresponds to its content?

awk '{ fname=$1 ".txt"; print > fname; close(fname) }' filename.txt


