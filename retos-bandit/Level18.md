# Level 18

## Objetivos
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

## Datos de acceso 
bandit17 <-UserName
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e<-Password

## Solución 
```bash
bandit16@bandit:/tmp$ ssh bandit17@localhost -i llave17 -p 2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Sep  1 06:30 .
drwxr-xr-x 49 root     root     4096 Sep  1 06:30 ..
-rw-r-----  1 bandit17 bandit17   33 Sep  1 06:30 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Sep  1 06:30 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Sep  1 06:30 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Sep  1 06:30 .ssh
bandit17@bandit:~$ diff passwords.old  passwords.new
42c42
< 09wUIyMU4YhOzl1Lzxoz0voIBzZ2TUAf
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```

## Notas dicionales 
Comando "diff" nos permite comparar archivos linea a linea