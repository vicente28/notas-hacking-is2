# Level 13

## Objetivos
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de acceso 
bandit12 <-UserName
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv <-Password

## Solución 

```bash
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cat data.txt  | xxd -r > /tmp/prueba/archivo.bin
bandit12@bandit:~$ cd /tmp/prueba
bandit12@bandit:/tmp/prueba$ ls
archivo.bin  data.gzip
bandit12@bandit:/tmp/prueba$ file archivo.bin
archivo.bin: gzip compressed data, was "data2.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix, original size modulo 2^32 575
bandit12@bandit:/tmp/prueba$ mv archivo.bin archivo.gz
bandit12@bandit:/tmp/prueba$ ls
archivo.gz  data.gzip
bandit12@bandit:/tmp/prueba$ gzip -d archivo.gz
bandit12@bandit:/tmp/prueba$ ls
archivo  data.gzip
bandit12@bandit:/tmp/prueba$ file archivo
archivo: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/prueba$ mv archivo archivo.bz2
bandit12@bandit:/tmp/prueba$ bzip -d archivo.bz2
Command 'bzip' not found, but there are 20 similar ones.
bandit12@bandit:/tmp/prueba$ bzip2 -d archivo.bz2
bandit12@bandit:/tmp/prueba$ ls
archivo  data.gzip
bandit12@bandit:/tmp/prueba$ file archivo
archivo: gzip compressed data, was "data4.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/prueba$ mv archivo archivi.gz
bandit12@bandit:/tmp/prueba$ gzip -d archivi.gz
bandit12@bandit:/tmp/prueba$ ls
archivi  data.gzip
bandit12@bandit:/tmp/prueba$ file archivi
archivi: POSIX tar archive (GNU)
bandit12@bandit:/tmp/prueba$ mv archivi arch.tar
bandit12@bandit:/tmp/prueba$ tar xf arch.tar
bandit12@bandit:/tmp/prueba$ ls
arch.tar  data5.bin  data.gzip
bandit12@bandit:/tmp/prueba$ rm arch.tar
bandit12@bandit:/tmp/prueba$ ls
data5.bin  data.gzip
bandit12@bandit:/tmp/prueba$ mv data
data5.bin  data.gzip
bandit12@bandit:/tmp/prueba$ mv data5.bin data5.tar
bandit12@bandit:/tmp/prueba$ ls
data5.tar  data.gzip
bandit12@bandit:/tmp/prueba$ tar xf data5.tar
bandit12@bandit:/tmp/prueba$ ls
data5.tar  data6.bin  data.gzip
bandit12@bandit:/tmp/prueba$ rm data5.tar
bandit12@bandit:/tmp/prueba$ ls
data6.bin  data.gzip
bandit12@bandit:/tmp/prueba$ mv data6.bin data6.bz2
bandit12@bandit:/tmp/prueba$ bzip2 -d data6.bz2
bandit12@bandit:/tmp/prueba$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/prueba$ mv data6 data6.tar
bandit12@bandit:/tmp/prueba$ ls
data6.tar  data.gzip
bandit12@bandit:/tmp/prueba$ tar xf data6.tar
bandit12@bandit:/tmp/prueba$ ls
data6.tar  data8.bin  data.gzip
bandit12@bandit:/tmp/prueba$ rm data6.tar
bandit12@bandit:/tmp/prueba$ mv data8.bin  data8.gz
bandit12@bandit:/tmp/prueba$ gzip -d data8.gz
bandit12@bandit:/tmp/prueba$ ls
data8  data.gzip
bandit12@bandit:/tmp/prueba$ cat data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

```

## Notas dicionales 
**Hex dump** is a [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal "Hexadecimal") view (on screen or paper) of computer data, from [memory](https://en.wikipedia.org/wiki/Computer_memory "Computer memory") or from a [computer file](https://en.wikipedia.org/wiki/Computer_file "Computer file") or [storage](https://en.wikipedia.org/wiki/Computer_data_storage "Computer data storage") device. Looking at a hex dump of data is usually done in the context of either [debugging](https://en.wikipedia.org/wiki/Debugging "Debugging") or [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).