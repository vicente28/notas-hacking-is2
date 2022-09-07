# Level 28

## Objetivos
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

## Datos de acceso 
bandit27 <-UserName
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS <-Password

## Solución 
```bash
	bandit27@bandit:~$ mkdir /tmp/vis
bandit27@bandit:~$ cd /tmp/vis
bandit27@bandit:/tmp/vis$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
bandit27@bandit:/tmp/vis$ cd repo
bandit27@bandit:/tmp/vis/repo$ ls
README
bandit27@bandit:/tmp/vis/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR

```

## Notas dicionales