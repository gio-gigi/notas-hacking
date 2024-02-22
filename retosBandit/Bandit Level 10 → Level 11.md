# Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

# Datos de acceso al nivel
username =  bandit10
password = G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
# Solución
```
bandit10@bandit:~$ whoami
bandit10
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "nos vamos" | base64
bm9zIHZhbW9zCg==
bandit10@bandit:~$
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
----SEGUNDA SOLUCIÓN:-----
bandit10@bandit:~$ python3
Python 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> cadena = open("data.txt").read()
>>> cadena
'VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==\n'
>>> base64
<module 'base64' from '/usr/lib/python3.10/base64.py'>
>>> base64.b64decode(cadena)
b'The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM\n'
>>>
```
# Notas adicionales
ctrl d : Me saca del interprete de python.
echo "" | base64 : Nos convierte una frase o palabras a base 64.
cat archivo | base64 -d : Nos ayuda a convertir en caracteres apartir de un archivo de base 64.
# Referencias