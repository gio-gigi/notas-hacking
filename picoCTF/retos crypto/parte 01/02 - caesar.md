# Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext).
# Pistas
1. caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)
# Solución

```
┌──(gio㉿kali)-[~/picoctf/criptografia/caesar]
└─$ wget https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
--2024-04-09 12:26:34--  https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                100%[===================================>]      35  --.-KB/s    in 0s      

2024-04-09 12:26:42 (51.8 MB/s) - ‘ciphertext’ saved [35/35]

                                                                                                      
┌──(gio㉿kali)-[~/picoctf/criptografia/caesar]
└─$ cat ciphertext 
picoCTF{dspttjohuifsvcjdpoabrkttds}   

ROT13
picoCTF{crossingtherubiconzaqjsscr}
```

```

```
# Notas adicionales
# Referencias
-  https://gchq.github.io/CyberChef/#recipe=A1Z26_Cipher_Decode('Space')&input=MTYgOSAzIDE1IDMgMjAgNiB7IDIwIDggNSAxNCAyMSAxMyAyIDUgMTggMTkgMTMgMSAxOSAxNSAxNCB9