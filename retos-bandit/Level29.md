# Level 29

## Objetivos
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso 
bandit28 <-UserName
AVanL161y9rsbcJIsFHuw35rjaOM19nR <-Password

## Solución 
```bash
bandit28@bandit:~$ mkdir /tmp/vis/
bandit28@bandit:~$ ls
bandit28@bandit:~$ cd /tmp/vis
bandit28@bandit:/tmp/vis$ ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
-bash: ssh://bandit28-git@localhost:2220/home/bandit28-git/repo: No such file or directory
bandit28@bandit:/tmp/priv$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...

bandit28@bandit:/tmp/vis$ ls
repo
bandit28@bandit:/tmp/vis$ cd repo
bandit28@bandit:/tmp/vis/repo$ ls
README.md
bandit28@bandit:/tmp/vis/repo$ cat README
cat: README: No such file or directory
bandit28@bandit:/tmp/vis/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/vis/repo$ git show
commit 43032edb2fb868dea2ceda9cb3882b2c336c09ec (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Sep 1 06:30:25 2022 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx
```

## Notas dicionales
Clonamos el repositorio en una carpeta nuestra, en el repositorio clonado  hay un readme, , recurrimos a hacer un "git show" que nos mostrara el ultimo cambio en el readme, donde mostrara la contraseña.