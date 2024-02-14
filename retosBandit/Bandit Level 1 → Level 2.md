# Objetivo
The password for the next level is stored in a file called **-** located in the home directory.

# Datos de acceso al nivel
username = bandit1
password = NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

# Solución
```
Primer intento mal:(
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$
Solución 1:
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
Solución 2:
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
# Notas adicionales
- Se aprendió hacer referencia a un archivo nombrad como un guión (-), hay que anteponer ./ para poder visualizarlo desde la cmd.
- pwd: nos permite visualizar la ruta del archivo.

# Referencias
- https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal
- https://www.google.com/search?q=dashed+filename