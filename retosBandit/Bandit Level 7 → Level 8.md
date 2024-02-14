# Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
# Datos de acceso al nivel
password = z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
username = bandit7
# Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ head data.txt
gallop  hu3ZhCrGRvfaO5jsY6ttvApzVCA2Hjvs
Aurelia's       ikl4F3cK5m6Cl6HAxva6zUAVJhI2Cvc6
stoicism        JiW9ts44udf20bJHe8H5dS1c99Muwz42
embodies        vWheZcAsQHZNnerI3ViW8wqOKIx0kbgR
Plato   dW2U8E5FfuAvNLdGDupP8GAxr922ZV0x
cultivation     A90E75jvWbEKrijFxM4GxqHEw8c8U2Bf
stable  omR4PHolFwbI0IEJsanveA21yWvFy8a7
bedspread       VlBFxuEDi3phEpljbKbahRJvJxfh3k9M
oppressing      hQTiEm5XF3cUQSEiBjh7sekemLOKBrcJ
darnedest       9O2zdCLKVoW5u34P9T7EKTZXcMRE6xh5
bandit7@bandit:~$ wc -l data.txt
98567 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# Notas adicionales
-  grep : Filtrar las líneas.
- wc : Cuenta las líneas de un archivo.
- head: Muestra las primeras líneas de un archivo.
- tail: Muestra las ultimas líneas de un archivo.
# Referencias
