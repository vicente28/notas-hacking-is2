# Level 9

## Objetivos
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso 
bandit8 <-UserName
cvX2JJa4CFALtqS87jk27qwqGhBM9plV <-Password

## Solución 

```bash

bandit8@bandit:~$ cat data.txt | sort | uniq -c
...
10 tVW9iY1Ml0uHPK4usZnN8oZXbjRt2ATY
10 U0NYdD3wHZKpfEg9qGQOLJimAJy6qxhS
10 UASW6CQwD6MRzftu6FAfyXBK0cVvnBLP
10 UJiCNvDNfgb3fcCj8PjjnAXHqUM63Uyj
10 UjsVbcqKeJqdCZQCDMkzv6A9X7hLbNE4
1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
10 UVnZvhiVQECraz5jl8U14sMVZQhjuXia
10 V2d9umHiuPLYLIDsuHj0frOEmreCZMaA

```

ó 

```bash 
bandit8@bandit:~$ cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## Notas dicionales 

comando "sort" me permite ordenar lineas 

comando "uniq" reporta u omite lineas repetidas 
	-c "las cuenta "
	-d "muestra la duplicadas"
	-u muestra solo la unica 