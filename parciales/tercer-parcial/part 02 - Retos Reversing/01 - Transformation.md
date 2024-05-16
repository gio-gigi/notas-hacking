# Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/1d8a5a2779c4dc24999f0358d7a1a786/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
# Pistas
1. You may find some decoders online
# Solución

```
┌──(gio㉿kali)-[~/tercerparcial/transformation]
└─$ cat enc          
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彥㜰㍢㐸㙽

┌──(gio㉿kali)-[~/tercerparcial/transformation]
└─$ python         
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.

>>> decode = '灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彥㜰㍢㐸㙽'
>>> print(decode.encode('utf-16-be'))
b'picoCTF{16_bits_inst34d_of_8_e703b486}'

```
# Notas adicionales
# Referencias
