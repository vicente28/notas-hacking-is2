# Level 3

## Objetivos
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso 
bandit2 <-UserName
boJ9jbbUNNfktd78OOpsqOltutMc3MY1 <-Password 
## Solución 

```bash

bandit2@bandit:~$ ls
spaces in this filename

bandit2@bandit:~$ cat "spaces in this filename"
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

ó

bandit2@bandit:~$ cat spaces\ in\ this\ filename
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

```

## Notas dicionales 

Para abrir un archivo con espacios en el nombre se puede usar comillas al inicio y al final del filename ó podemos utilizar diagonales invertidas 