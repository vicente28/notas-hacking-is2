# Level 15

## Objetivos
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de acceso 
bandit14 <-UserName
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq<-Password
## Solución 

```bash
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```

## Notas dicionales 
 
nc host puerto se conecta a un host en un puerto determinado 

nos pedira la contraseña de este nivel, el encontrado en el nivel anterior 