# Level 5

## Objetivos
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso 
bandit4 <-UserName
pIwrPrtPN36QITSp3EQaw936yaFoFgAB <-Password

## Solución 

``` bash

bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
/`2ғ%rL~5g��

bandit4@bandit:~/inhere$ file ./-file00
./-file00: data
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data

bandit4@bandit:~/inhere$ cat ./-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh





```

lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
## Notas dicionales 
Usamos el comando "File" seguido del nombre (OJO como el nombre inicia con "-" ponemos "-/ para poder abrirlo") así sabremos que tipo de contenido tiene un archivo. 

usamos "[*]" para mostrar todos y no, uno por uno: "[file ./*]"