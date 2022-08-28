# Level 10

## Objetivos
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso 
bandit9 <-UserName
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR <-Password

## Solución 

```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ cat data.txt | strings | grep ==
========== the*2i4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

## Notas dicionales 

comando "strings" me permite imprimir cadenas de un archivo  binario

comanndo "grep == " filtramos las palabras que aparecieran las palabras que contengas con doble guion 