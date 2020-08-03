# Useful lines of code
---
## Table of Contents
- [scp-ing files from a list](#scping-files-from-a-list)
## scping files from a list
`while read file; do scp "user@host:$file" .; done < files`
or if you're prompted to 
`while read file; do scp "user:password@host:$file" .; done < files`
[Credits - Gal Red Jelly Kauffman on Stack Overflow](https://stackoverflow.com/questions/26454654/ssh-scp-files-from-a-list)

