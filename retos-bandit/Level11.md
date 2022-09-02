# Level 11

## Objetivos
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso 
bandit10 <-UserName
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk <-Password

## Solución 
```bash
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```


ó

```bash
bandit10@bandit:~$ python3
>>> f=open('data.txt', 'r')
>>> mensaje = f.read()
>>> codecs.decode(mansaje,'base64')
>>> The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

```


## Notas dicionales 
base 64
es un [sistema de numeración](https://es.wikipedia.org/wiki/Sistema_de_numeraci%C3%B3n "Sistema de numeración") [posicional](https://es.wikipedia.org/wiki/Notaci%C3%B3n_posicional "Notación posicional") que usa 64 como base. Es la mayor potencia que puede ser representada usando únicamente los caracteres imprimibles de [ASCII](https://es.wikipedia.org/wiki/ASCII "ASCII").

usan el rango de caracteres A-Z, a-z y 0-9

el comando  "base64" codifica y  con "-d" nos permite decodificar