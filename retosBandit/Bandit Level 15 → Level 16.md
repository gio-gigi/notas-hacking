# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

# Datos de acceso al nivel
username = bandit15
password = jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
# Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEIivS1jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC4
XC9dgne8ha9I/vXn4uTtObLhI/PPyLyl4jyDQPp61VtsEMcOb95KhXxdtQiDtzSD
3KXQVFLaPlVGKDWSR9nV+GoazSNPmNLH/IMVrUYxXjYikPxo1jjYKyuqfjV5bNm3
Hz6z4eDl7wNbPRaPAMPo0WU23m9M04bKQHLINfN7Abz3a+7ChLeICrWXiXp9mWfj
PY8cK7Vayz0eHU4Lg64q4jUaXQqZ/ta1RqZEwv7ZuTKctcazpK/u2+h4zvQCPyLh
uDjUXZTLlIuhfjyKUJLQsmYHAQprV6sY3ybFN32dW6MSE0/ApT6Th0LzKeaYxk5b
3NIeaYyPeKsjqFSwy+2zAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBQ
RXG1k+cB357X43fsiyaCQQh4RbWHOcg1jBes5eiC/H8MyC3ec1znXvOUfqJcWNQJ
9UJDMwbkpo+IcwJiOe9n/D3Zeypv1g+ta8KKLsQ+zcbp5RdltKy7GuO/s5WjVofE
/IHz/5g+IMoqqYLlquQ539CZykPMC9TB9uWfJj/i8faCox4gjtkSCri+27tUZuHi
eYR3zxY1ptsJti/pMaItC6Oc2/pSlotQ4fXdciLZYGXqlmSFBt8Y8/v1YkhME5gN
3HmBV/Zg1SghA57zYsbf3npvQwudr04f2iF493pe0VRN6DfiXTxWkJe1VKuyGHEr
Q4L4OdVlgMSeyYyKgFc7
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
    Session-ID: 2C9ADD32A795D92FAFA4AD91E03F086D7AF4DD70DFB59C49F1EDD82ACA58FE19
    Session-ID-ctx:
    Resumption PSK: AC34603B7307BFA679CE3079ACFB0C111DD14D677947950EE9126FEB30D77E2F6B2CA87DCC71C0B198E00180DF6EEEF7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - f5 25 c3 71 38 87 a9 4b-84 29 0e 2e 0d 1b 32 6f   .%.q8..K.)....2o
    0020 - ff de a0 bf bf 8e 8c 49-0b 5f 16 e7 d2 db b5 43   .......I._.....C
    0030 - f3 7d 98 18 8b 2e 59 fb-75 42 d6 2c d5 76 b8 ba   .}....Y.uB.,.v..
    0040 - b8 37 e6 02 f7 e9 02 50-04 c0 af 03 36 bb 02 13   .7.....P....6...
    0050 - cf ea 0f 27 67 fb 26 a0-d4 af ce 13 fb 58 4e 95   ...'g.&......XN.
    0060 - 40 ff 82 d2 3c 7d c0 23-26 0b 80 8a b0 3d a0 c8   @...<}.#&....=..
    0070 - 87 6d 29 7c cf 60 45 13-c7 20 be 66 6a 3c bb 68   .m)|.`E.. .fj<.h
    0080 - 43 8f 9d 27 d4 89 e8 d5-de 2c 56 51 d2 47 bd a1   C..'.....,VQ.G..
    0090 - 9b fe 25 2c fd e8 e0 90-92 27 c6 26 9f c7 21 7e   ..%,.....'.&..!~
    00a0 - 00 cd f4 c4 a6 d4 e6 d4-17 32 d5 8a ef 38 f6 7d   .........2...8.}
    00b0 - b8 33 5c 21 7a d8 74 37-03 01 7f 76 ab bb 46 9f   .3\!z.t7...v..F.
    00c0 - 13 43 e8 5d 6e cf a1 c0-82 bc ed 5f ab 2b d1 70   .C.]n......_.+.p

    Start Time: 1708457256
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
    Session-ID: BF4C00AC97C3D91EC1EA02B95A6907467F08BAB59DA47574D694FF2309C9E441
    Session-ID-ctx:
    Resumption PSK: DA6F1D18A09A124578C2D710A0DF9784263E9D4B72BDF602706DC1E630492B2C2C5510A092050649862791673E98FCBA
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - 17 a6 76 c9 c2 52 bf 00-72 e9 18 62 f6 86 d7 27   ..v..R..r..b...'
    0020 - 24 7a 88 c9 18 18 1e 2f-72 dc f8 6f 0e c2 7c 44   $z...../r..o..|D
    0030 - d2 1a 25 25 4b 09 d8 5f-cc 82 1b 79 cc 44 f2 94   ..%%K.._...y.D..
    0040 - 51 a1 4f e0 3d f4 bd 98-3b cd e4 21 78 12 38 f7   Q.O.=...;..!x.8.
    0050 - c9 e1 84 e5 96 a4 3b 40-2b 63 f6 7c 15 8e f0 cd   ......;@+c.|....
    0060 - 93 ee 3d 3a a6 eb f1 77-5e 6e 5c ab dd a4 04 5c   ..=:...w^n\....\
    0070 - c3 cf f8 2b 1b 7d 10 15-a5 82 37 a3 2b bd 7a 8c   ...+.}....7.+.z.
    0080 - 16 ce 58 93 a9 6d a3 ea-6c 66 75 b3 3d ef 63 24   ..X..m..lfu.=.c$
    0090 - 1e a3 77 5a f9 11 3d f5-4b 56 11 80 b4 8a d6 a0   ..wZ..=.KV......
    00a0 - 9f 9a 62 97 4a 7e 9a 76-3a 29 5a 2d 42 60 4b aa   ..b.J~.v:)Z-B`K.
    00b0 - b8 24 bb b3 cb 2d 6f 30-a4 e6 58 b0 1f b4 68 d3   .$...-o0..X...h.
    00c0 - 36 ff 54 bf 90 d4 71 4a-db d6 39 6a 87 1f 56 46   6.T...qJ..9j..VF

    Start Time: 1708457256
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
# Notas adicionales
openssl s_client -connect : un puerto que habla ssl
Certificado digita: Es un certificado para validad que es seguro.
# Referencias