# Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.
# Pistas
1. What is a hex editor?
# Solución
```
──(gio㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
--2024-03-12 12:15:42--  https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[================>]   2.19M  1.98MB/s    in 1.1s    

2024-03-12 12:15:45 (1.98 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                             
┌──(gio㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ ls         
garden.jpg
                                                                             
┌──(gio㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ open garden.jpg
┌──(gio㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ strings -n 10 garden.jpg    
ae:uc(>YwG
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"
┌──(gio㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ strings -n 10 garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"
```
# Notas adicionales
# Referencias