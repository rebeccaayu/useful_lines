# Useful lines of code
---
## Table of Contents
- [file transfer](#working-with-remote-things)
	- [scp-ing files from a list](#scping-files-from-a-list)
	- [rsa keys](#rsa-keys)

## Working with remote things
### scping files from a list
For the times when you have a list of files you want to transfer and don't want to do it manually:
```
while read file; do scp "user@host:$file" .; done < files
```
or if you're prompted to enter your password every time: `while read file; do scp "user:password@host:$file" .; done < files` but you should probably just add your [rsa key](#rsa-keys) then.
[[Credits - Gal Red Jelly Kauffman on Stack Overflow](https://stackoverflow.com/questions/26454654/ssh-scp-files-from-a-list)]

### RSA keys
```
rsa-keygen
~/.ssh/authorized_keys
cat ~/id_rsa.pub >> ~/.ssh/authorized_keys
```
