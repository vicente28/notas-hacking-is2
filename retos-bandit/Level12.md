# Level 12

## Objetivos
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso 
bandit11 <-UserName
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM <-Password
## Solución 
```bash
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```

ó

```bash
bandit11@bandit:~$ python3
.
>>> import codecs
>>> f=open('data.txt', 'r')
>>> mensaje=f.read()
>>> codecs.decode(mensaje, 'rot13')
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv'
```
## Notas dicionales
**ROT13** («**rotar 13 posiciones**») es un sencillo [cifrado César](https://es.wikipedia.org/wiki/Cifrado_C%C3%A9sar "Cifrado César") utilizado para ocultar un texto sustituyendo cada letra por la letra que está trece posiciones por delante en el [alfabeto](https://es.wikipedia.org/wiki/Alfabeto "Alfabeto")

Aplicar el ROT13 a un texto se reduce a examinar sus caracteres alfabéticos y sustituirlos por la letra que está 13 posiciones por delante en el alfabeto, volviendo al principio si es necesario y conservando las mayúsculas y minúsculas: