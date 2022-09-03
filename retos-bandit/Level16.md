# Level 16

## Objetivos
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de acceso 
bandit15 <-UserName
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt<-Password

## Solución 

```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  1 06:31:12 2022 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  1 06:31:12 2022 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  1 06:30:12 2022 GMT; NotAfter: Sep  1 06:31:12 2022 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEHn8h8jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjIwOTAxMDYzMDEyWhcNMjIwOTAxMDYzMTEyWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDK
u/UD6yArwj259J4o2IVQQGvM/oGVIiYYppFd1jxltmQ03SOUVg+4px+7qOJuCbxA
AH9NCAl55r7v/VDlwGkpu4c2GaqR3zSAlidrtJjrVFZP/QilXdv0uV35N4i30BuT
DdI+FzlYcQx7ztZdtDxp61FTjET4BIcFmSzMQLitpYeeiVcKLXTPnsF8216drWjQ
0Ucb+3RvGgPo/rKPra8/7WYFa8ALdnu2rwP07ndtMDL3iJF9VMuBsr8UuTdsktwa
174QGx0f3RFkcKJ1foxYnSoHvy0BhxVGguMKuinY6cyLELwnjcAp4A2oGI438GnV
whe39ZlCkGved612QLhDAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQDE
2X2mgxYDvujnIAL2Qbs8JnUBFe3lZsRZJbPgko3MZ4lScB5Rbz+vb6q6s0KGGMjh
sKweg4BtG4sQWDIwX2yd4XwJa8rrGWuoA4kgCQ/jJhFZrbCPbDN3sbzX8Tql+epd
oJyQcvLOkWDazRPgx0i4dMXIgUv0kbE+NCvj2waXHldMyjT6GFL2bdv/Xd8ffnXg
wlggJKKIzl0RMp/5z5n1bPMoLVl5HcUG3UzOsTcqcSThTr3JXeWLjaL0qJfAfcw5
V+GM2tGTQB3c4jvISAl5RAARpvFUMc4d4hKd6aesRcFHZfbtSjxglPFmeL1VGxJ9
EIg5c/xwHOE6dgDA2WdS
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
    Session-ID: C21869A2232A7FAA1670FF97846BDF31042914A7236D996ED1202B4B78D6AFEA
    Session-ID-ctx:
    Resumption PSK: E45E699599D06D205FAA4325BEDB4E8903CBD231DA3885C716C0A2B1D961E1736E62473CEF5ADBF44637D1BCE16AA0E2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 86 a0 aa 25 48 38 1d-0e b1 8d f8 fa 82 ac 33   ....%H8........3
    0010 - 62 ef 87 8c a9 00 3e aa-72 ef a0 dc 95 38 06 2a   b.....>.r....8.*
    0020 - b6 18 20 70 f9 f4 3b 6c-3b b9 4a 2e d0 ce 27 77   .. p..;l;.J...'w
    0030 - 0b da 99 35 5c b6 e4 a0-59 a7 d3 2d c6 33 f7 5b   ...5\...Y..-.3.[
    0040 - 23 2b 8d f7 1e cd 65 49-86 46 96 77 c9 fe a6 d1   #+....eI.F.w....
    0050 - 19 e5 92 ea 93 0c 1b 52-57 a8 a5 0d 2e 64 c9 62   .......RW....d.b
    0060 - 85 a3 93 ba ca d8 8c 68-8f bd 98 2d 3b fb c4 86   .......h...-;...
    0070 - 6c 3f 2e c4 8a 61 cd 48-7b cd f3 68 26 61 e2 d0   l?...a.H{..h&a..
    0080 - 9e a8 b9 82 80 70 dd 47-20 60 89 ef ec 7f ce 16   .....p.G `......
    0090 - 3d c5 96 a1 4f ae b5 a7-80 65 7f ce 23 7e 00 cd   =...O....e..#~..
    00a0 - a2 b7 36 13 ba 48 78 4d-df 04 95 42 21 91 9f 49   ..6..HxM...B!..I
    00b0 - f6 67 e3 f5 48 e3 14 1d-dd 15 af fe 99 07 0e 86   .g..H...........
    00c0 - 77 28 5a 8f db 93 00 54-27 bd 0a 4a 35 c1 17 61   w(Z....T'..J5..a

    Start Time: 1662181801
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
    Session-ID: DD74E5ACC79F4996ED59E27E4CA3C840F4B4C3DADCBB15125098AFEC4994E9AD
    Session-ID-ctx:
    Resumption PSK: EAC5741D3ED7468625C84C9A4B6CFD41D4BA4E1759C5CA7C77199A6E20A45EAA5A575E2D36AC3D2AFE5F82D1D2E777B0
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 86 a0 aa 25 48 38 1d-0e b1 8d f8 fa 82 ac 33   ....%H8........3
    0010 - 7b 8c fb f5 b6 cd 40 02-4c 5f f0 10 77 48 67 b1   {.....@.L_..wHg.
    0020 - 62 e6 41 15 e7 a5 0e d8-27 fc f9 2c a1 36 14 05   b.A.....'..,.6..
    0030 - d8 34 d8 01 b0 10 17 fa-8a 8a 98 61 a9 dc 15 4c   .4.........a...L
    0040 - 85 d1 64 08 ea 96 e9 01-e7 b8 db 5d 28 5d d8 23   ..d........](].#
    0050 - ea 1c 00 42 c6 8d 99 81-02 20 eb b1 f7 8a 21 14   ...B..... ....!.
    0060 - 77 a4 fb 7b 44 49 6d 2b-14 2b 96 2b 39 db 0d b8   w..{DIm+.+.+9...
    0070 - 3d 2f 7f c9 82 fe 51 5a-78 be d4 e8 0b c5 1a df   =/....QZx.......
    0080 - 62 66 73 c2 57 3d 80 b1-21 d8 62 d8 68 14 73 21   bfs.W=..!.b.h.s!
    0090 - 79 a9 b0 19 7f d5 1e eb-d8 a3 ea 60 a3 53 a0 44   y..........`.S.D
    00a0 - e9 fd 7d f4 4e 6c 9d 18-50 74 38 1a 96 ae 2a 8f   ..}.Nl..Pt8...*.
    00b0 - 5d 5a 30 b9 65 95 fc e7-38 84 19 47 d0 9f 78 ca   ]Z0.e...8..G..x.
    00c0 - 9a 0d 61 1d d8 2e 0b f7-4d c9 a5 86 6d e7 88 4c   ..a.....M...m..L

    Start Time: 1662181801
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
```

## Notas dicionales 
SSL **proporciona autenticación y privacidad de la información entre extremos sobre Internet mediante el uso de criptografía**. Habitualmente, solo el servidor es autenticado mientras que el cliente se mantiene sin autenticar.
Son [protocolos criptográficos](https://es.wikipedia.org/wiki/Protocolo_criptogr%C3%A1fico "Protocolo criptográfico"), que proporcionan comunicaciones seguras por una red comúnmente internet

OpenSSL es una implementación de código abierto de los protocolos de Capa de sockets seguros (SSL) y del protocolo Transport Layer Security (TLS) que aseguran las comunicaciones en la red.

$ openssl s_client – connect [yourdomain].com:443 así nos conectamos a un en un puerto ssl
