# Level 31

## Objetivos
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de acceso 
bandit30 <-UserName
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS <-Password
## Solución 
```shell
bandit30@bandit:~$ mkdir /tmp/vis/
bandit30@bandit:~$ cd /mkdir/vis
-bash: cd: /mkdir/dir: No such file or directory
bandit30@bandit:~$ cd /tmp/vis
bandit30@bandit:/tmp/vis$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
bandit30@bandit:/tmp/dir$ ls
repo
bandit30@bandit:/tmp/vis$ cd repo
bandit30@bandit:/tmp/vis/repo$ ls
README.md
bandit30@bandit:/tmp/vis/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/vis/repo$ git show
commit a325f29e1cc26b0f0dc5f89b4348e389b408cc87 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Thu Sep 1 06:30:28 2022 +0000

    initial commit of README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..029ba42
--- /dev/null
+++ b/README.md
@@ -0,0 +1 @@
+just an epmty file... muahaha
bandit30@bandit:/tmp/vis/repo$ git tag
secret
bandit30@bandit:/tmp/vis/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/vis/repo$

```

## Notas dicionales
Clonamos un repositorio, abrimos el readme, hacemos uso del "git tag", y nos muestra "secret" lo mostramos con  "git show secret" .
Hacemos uso de 
		-git tag
		-git show