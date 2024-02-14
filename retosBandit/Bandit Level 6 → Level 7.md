# Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
# Datos de acceso al nivel
username = bandit6
password = P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
# Solución
```
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
............. infinito
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# Notas adicionales
- El 2>/dev/null -> Manda la salida de error al dispositivo nulo (no aparece en pantalla)

# Referencias