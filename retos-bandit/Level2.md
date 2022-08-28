# Level 2

## Objetivos
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso 
bandit1 <-UserName
boJ9jbbUNNfktd78OOpsqOltutMc3MY1 <-Password 

## Solución 
``` bash 

bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@bandit:~$

```

ó 

``` bash 

bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1

bandit1@bandit:~$ cat /home/bandit1/-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9


```




## Notas dicionales

' - ' es un nombre de archivo que si queremos abrir con cat por si solo no se abrirá 
 Tendremos que usar  './' y nombre de archivo  de la siguiente manera: 
 
 cat ./-  

tambien escribiendo la ruta completa (si no la conocemos comando 'pwd ' para ver la ruta )
y quedaría de esta forma: 

cat /home/bandit1/- 