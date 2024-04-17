# Objetivo
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/425/readmycert.csr).
# Pistas
1. Download the certificate signing request and try to read it.
# Solución
```
ubuntu@ip-172-31-46-190:~/gio/readmycert$ cat readmycert.csr
-----BEGIN CERTIFICATE REQUEST-----
MIICpzCCAY8CAQAwPDEmMCQGA1UEAwwdcGljb0NURntyZWFkX215Y2VydF82OTNm
N2MwM30xEjAQBgNVBCkMCWN0ZlBsYXllcjCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAPp+XuDB3ZkmrkvAsgtjP+mjIcYDWfptuZsJieu6eRl39wl4Sg38
+/OfY24LV9sNmgKyTGvpmCaUoZMYkvkulYSoFzE0xqPBo6kruLEyIvqqpAFqRH2b
mierLT6RcKgJHYr/Vt6SwP8NCCawCrvhQ4NZcuB49Hr/2AiGHzmf86/lG/c+lhmH
gyqPb1kDghsVxi/GNs9i7AgniZikqT8OTp0INmmCgZtJn1Jo615Iu/tFiC8Sfhhg
QHmTDLjgx1oP1kvZV2PE5UUN/oC05Zup8f31LksXZwpazZKwYC/LbN96HdqgVQ9K
S8e/4I7MJQmPmLIsLp3sdL2FiDGML3smAi0CAwEAAaAmMCQGCSqGSIb3DQEJDjEX
MBUwEwYDVR0lBAwwCgYIKwYBBQUHAwIwDQYJKoZIhvcNAQELBQADggEBAOxSR8Fs
Tdjfu9e0vRNqKWd09ISmYDQc3qnSbLRlYZyMK4pguALq310h/1nNgURWESbNJPOp
FkBWG0XWhWyWP7rTqxo/pk9AKx0TNbHDrS6KiBnKPq0mxjPZsH1L7wNYDc5OANDl
btvn3zT7lMms6z1qM7xUWXR76n2xL/81cdF725nBZ00mWmPW0S1pSmA4EEHCEgNW
0vWQqsIDki3gYc4NCm8OHjx79kcwE+ksyc6vHgMOwsYoOFJnyayhl15oN/3x7hW3
G1xovPupABpfOSNOcTwbgfrfjUDOLx/wirvj9L1N5EGDh4FOLaRZDs+tMrimGBBS
zGU13BnykmQ5jOQ=
-----END CERTIFICATE REQUEST-----
ubuntu@ip-172-31-46-190:~/gio/readmycert$ openssl req -text -noout -verify -in readmycert.csr
Certificate request self-signature verify OK
Certificate Request:
    Data:
        Version: 1 (0x0)
        Subject: CN = picoCTF{read_mycert_693f7c03}, name = ctfPlayer
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (2048 bit)
                Modulus:
                    00:fa:7e:5e:e0:c1:dd:99:26:ae:4b:c0:b2:0b:63:
                    3f:e9:a3:21:c6:03:59:fa:6d:b9:9b:09:89:eb:ba:
                    79:19:77:f7:09:78:4a:0d:fc:fb:f3:9f:63:6e:0b:
                    57:db:0d:9a:02:b2:4c:6b:e9:98:26:94:a1:93:18:
                    92:f9:2e:95:84:a8:17:31:34:c6:a3:c1:a3:a9:2b:
                    b8:b1:32:22:fa:aa:a4:01:6a:44:7d:9b:9a:27:ab:
```
# Notas adicionales
# Referencias
- https://pleasantsolutions.com/info/pleasant-password-server/b-server-configuration/3-installing-a-3rd-party-certificate/openssl-commands