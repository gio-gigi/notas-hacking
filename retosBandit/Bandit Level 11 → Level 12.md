# Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

# Datos de acceso al nivel
username = bandit11
password = 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

# Solución
```
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
----Otra solución---
bandit11@bandit:~$ python3
Python 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> cadena = open("data.txt").read()
>>> codecs.decode(cadena,"rot13")
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv\n'
```
# Notas adicionales
ROT13 : Rota 13 veces.
tr : Transformar
# Referencias
- https://en.wikipedia.org/wiki/ROT13
- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=R3VyIGNuZmZqYmVxIHZmIFdJQU9PU0Z6TWpYWEJDMEtvU0tCYko4cHVRbTVsSUVp
