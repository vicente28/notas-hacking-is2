# Level 8

## Objetivos
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de acceso 
bandit7 <-UserName
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs <-Password

## Solución 

```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
bandit7@bandit:~$ cat data.txt  | grep millionth
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV

```

## Notas dicionales 

"grep" nos permite buscar un patron en el archivo 

" | " nos redirge la salida 