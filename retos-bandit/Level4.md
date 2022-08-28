# Level 4

## Objetivos
The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso 
bandit3 <-UserName
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK <-Password 

## Solución 
``` bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ man ls
bandit3@bandit:~/inhere$ bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~/inhere$
```

## Notas dicionales 

Con el comando "man" que es el manual podemos solicitar ayuda del comando ls 
aquí encontramos que el comando "-a " nos permite mostrar archivos ocultos como es el caso