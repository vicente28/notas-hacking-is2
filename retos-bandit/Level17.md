# Level 17

## Objetivos
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso 
bandit16 <-UserName
JQttfApK4SeyHwDlI9SXGR50qclOAil1<-Password
## Solución 

```bash
bandit16@bandit:~$ nmap -p31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2022-09-03 05:18 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000096s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  1 06:31:13 2022 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  1 06:31:13 2022 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  1 06:30:13 2022 GMT; NotAfter: Sep  1 06:31:13 2022 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEaysfcTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjIwOTAxMDYzMDEzWhcNMjIwOTAxMDYzMTEzWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCW
SLI0BBG+QwOrlYF7amECTNwYr0o8pAzI0D9nA7ENSZ3iQQrPH+OKeFJoYpzg2D+C
eDBIdZbUl+gNF0pb0nlwosHePsoezlk+i7Al3WoICiUN9mc09YVEViI9jVcOcGzO
TZIbeCsmGbvYTN75qXzZ5EqfySHNWwEV8CuOml+VTVlBiteSK76soKuZzTFPRDUB
NOJkO/ZDUpmCZJ0d4Zv6A2+qeuwNCF5OqH+OF2rAwQIKO6oEYPQGDuWlm+WWEF6P
3fz0wnu+ir44iVDYAb37FvsaSgayo5CLmwOsjB/68+lnTgatvnJLVbR3i33hpirV
3QOkkffspxg6veqkjaFFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBW
/dHgi5TmckCJQclZmOus7FfwwkURutv4BkmWQYGGg4uxgIvTjp3n3k74w0/InnRR
rJQFtRxWcRsuFnheXfW+cZ6n6nZIDgEzI2iLRjy9b5vQDkqK4xL44sWe4/C11D4a
6oYkoBmhWOoKbjHiEiYUMY+iRhbN6EYf18RjsRE7utDfj0KMG2d0EsBDzyBO25un
G/LxkQG1Kr17pf/KFgYifZaCYIFy9uJ/pOqDMJCiMuqpNPjJ0yyLb1FReU9LOm5U
qARBeYIC6kPP8H/tbgT3KHCfp80PTS75feD80UztCOB9gfsrVnoptyN9cc4+jLgm
K0UL8LZEUDnsrDByEcgr
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: A830D6CE848D99F19B646D799EE70E938998637A5D67A6D012888E1639F5F59C
    Session-ID-ctx:
    Resumption PSK: 173FD167CA7F3FC3BFE408C122518EF3DDC9C3A5996094EEA214F61C1AAAE835030B1949B436445ADC6CE531A59557C1
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 05 ad 43 95 c3 32 2b 84-06 ed 98 c0 bc b4 c3 e3   ..C..2+.........
    0010 - 40 e7 05 fb 10 fe f3 26-06 65 84 bd d7 c3 7f 08   @......&.e......
    0020 - 7c d4 4d 62 a8 b4 30 0a-3d 7f 11 32 af ce f9 7b   |.Mb..0.=..2...{
    0030 - e4 a0 22 14 10 be 31 bb-c5 38 38 af c7 c3 7f f3   .."...1..88.....
    0040 - 81 16 36 94 cd c2 6a 67-de c9 f9 56 c2 e5 a5 8b   ..6...jg...V....
    0050 - d6 fd 70 a4 cf 7c 2a f6-58 2f 69 f5 8e a5 f2 01   ..p..|*.X/i.....
    0060 - 9b db ea 41 fa 45 16 59-d9 eb 45 38 4f e8 14 db   ...A.E.Y..E8O...
    0070 - 73 9e 45 04 64 d3 2a a8-5f f3 5e 92 af 86 54 1b   s.E.d.*._.^...T.
    0080 - e6 a9 0b fb 9f e0 3e 91-78 d6 fb 97 27 bd 8b 2e   ......>.x...'...
    0090 - 0c 52 17 c1 19 bb 24 2b-af ef d9 78 d6 df 75 92   .R....$+...x..u.
    00a0 - 12 5d 50 8f c1 c6 a8 c8-22 3d 57 8b d7 6b 45 4f   .]P....."=W..kEO
    00b0 - 05 a3 de bc 6b c4 86 3a-42 d0 aa 56 8e 61 2b d4   ....k..:B..V.a+.
    00c0 - 3b cb e9 6c 74 2b 19 0b-5a 20 6f 0e 18 23 ef 4f   ;..lt+..Z o..#.O

    Start Time: 1662182556
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 3F05404C32CE15B1246A4EBB0E646B65692F2D0AAF3131E70C18A99CB99AA59B
    Session-ID-ctx:
    Resumption PSK: EA251A6BD64F2BCE664B489F23E761A175A85ABE01570BA9DDE0A1A601AD73586C76E4EE263BB7B58A672131CA1DAAB5
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 05 ad 43 95 c3 32 2b 84-06 ed 98 c0 bc b4 c3 e3   ..C..2+.........
    0010 - fe 11 90 4a cd 41 ff 57-99 a0 03 fd 6d 80 af 1f   ...J.A.W....m...
    0020 - ee 3d 2b f0 8d 5a 49 3c-50 f1 89 8f b4 44 9a 96   .=+..ZI<P....D..
    0030 - f3 cc 60 7f 73 31 b9 12-a1 f3 e6 81 65 a1 93 97   ..`.s1......e...
    0040 - 0b 89 a2 f7 d6 a8 0b 96-ca f7 75 df a2 86 2a 0f   ..........u...*.
    0050 - 71 42 7b 74 95 5e ed ad-cd 2c e3 4a 7d 54 34 e5   qB{t.^...,.J}T4.
    0060 - 7f b8 c6 c7 0f ae b0 0f-e7 23 74 c3 f0 72 54 27   .........#t..rT'
    0070 - 27 20 ff 1f c5 ce a2 5d-8d cb a7 b1 0d 3d 2d ff   ' .....].....=-.
    0080 - c3 63 34 b4 bf 28 02 20-73 95 9e b8 d2 71 1e db   .c4..(. s....q..
    0090 - 78 e5 a2 ba 49 0f bb 32-ec 51 9a 52 79 76 a4 f1   x...I..2.Q.Ryv..
    00a0 - cd 08 5f ca 01 15 6c 6a-92 1f 5d 8f 9e a0 84 12   .._...lj..].....
    00b0 - 64 de c5 b9 5d 5a 06 e6-e0 c1 17 26 c1 45 69 ca   d...]Z.....&.Ei.
    00c0 - 6a 5c 64 8b 63 50 11 3f-1c 83 54 2e 99 cd 3f 0d   j\d.cP.?..T...?.

    Start Time: 1662182556
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-
```

## Notas dicionales 
Un escaneo de puertos o portscan es un proceso que envía solicitudes de clientes a un rango de direcciones de puerto de servidor en un host, con el objetivo de encontrar un puerto activo;  La mayoría de los usos de un escaneo de puertos no son ataques, sino sondeos simples para determinar los servicios disponibles en una máquina remota.

"nmap" es un comando que me permite escanear puertos con el agregado "-p" podemos definir el rango 