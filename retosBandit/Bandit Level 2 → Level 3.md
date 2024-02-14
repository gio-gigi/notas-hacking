# Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory.

# Datos de acceso al nivel
password = rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
username =  bandit2

# Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# Notas adicionales
- Cuando hay espacios en los nombres de archivos, podemos usar:
	- Encerrar el nombre entre comillas ("").
	- Hacer uso de diagonal invertida.
# Referencias
- https://linuxhandbook.com/filename-spaces-linux/