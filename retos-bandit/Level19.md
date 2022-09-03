# Level 19

## Objetivos
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Datos de acceso 
bandit18 <-UserName
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg<-Password
## Solución 
```bash
C:\Users\estel>ssh bandit18@bandit.labs.overthewire.org -p 2220 "/bin/bash"


ls -la
total 24
drwxr-xr-x  2 root     root     4096 Sep  1 06:30 .
drwxr-xr-x 49 root     root     4096 Sep  1 06:30 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r-----  1 bandit19 bandit18 3794 Sep  1 06:30 .bashrc
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
-rw-r-----  1 bandit19 bandit18   33 Sep  1 06:30 readme
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

## Notas dicionales 

Al intentar ingresar como normalmente lo hacemos , nos permite entrar pero inmediatamente nos saca 

Agregado al final "bin bash" al momento de logearnos ya no se sale, y podemos ejecutar el bash aunque no tenga promt  