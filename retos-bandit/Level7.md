# Level 7

## Objetivos
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso 
bandit6 <-UserName
DXjZPULLxYr17uwoI01bNLQbtFemEgo7 <-Password
## Solución 

```bash
bandit6@bandit:~$
bandit6@bandit:~$ ls
bandit6@bandit:~$ pwd
/home/bandit6
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/root’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
f.......
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>dev/null
-bash: dev/null: No such file or directory
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
bandit6@bandit:~$
```

## Notas dicionales 
comando "find -user" puedo buscar por usuario, con "find group" puedo buscar los grupos 

Uso de File Descriptors 
	0 <-stdin      Entradas de consola 
	1 <-stdout    Output consola
	2 <-stderr     Errores en consola

"2>/dev/null" con esto decimos que los errores nos los mande o rediriga a null para eliminar la salida de errores 