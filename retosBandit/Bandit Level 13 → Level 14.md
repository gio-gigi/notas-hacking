# Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
# Datos de acceso al nivel
username = bandit13
password = wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
# Solución
```
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p2220
bandit14@bandit:~$ cat /etc/bandit_pass/bandit1
cat: /etc/bandit_pass/bandit1: Permission denied
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
# Notas adicionales
La importancia de las llaves privadas y su uso.
# Referencias