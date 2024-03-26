# Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static)? This [BASH script](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh) might help!

# Pistas

# Solución
```
giogi-picoctf@webshell:~$ ls
README.txt  flag  flag.1  ltdis.sh  static  warm
giogi-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh
--2024-02-27 19:11:37--  https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh.1'

ltdis.sh.1                   100%[==============================================>]     785  --.-KB/s    in 0s      

2024-02-27 19:11:37 (229 MB/s) - 'ltdis.sh.1' saved [785/785]

giogi-picoctf@webshell:~$ strings static | grep
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
giogi-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_ae0b3ef2}
```
# Notas adicionales
# Referencias