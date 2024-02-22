# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

# Datos de acceso al nivel
username = bandit14
password = fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
# Solución
```
-------PRIMERA SOLUCIÓN-----
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

--------SEGUNDA SOLUCIÓN-----
bandit14@bandit:~$ echo "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq" | nc localhost 30000
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

--------TERCERA SOLUCIÓN-----
bandit14@bandit:~$ nc localhost 30000 <<<  "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq"
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

```
# Notas adicionales
nc : para entrar a un puerto, o conectarme a un servidor o puerto especifico.
# Referencias