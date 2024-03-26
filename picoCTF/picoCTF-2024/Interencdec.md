## Objetivo
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/108/enc_flag).
## Solución

```
vagrant@ubuntu-jammy:~$ ls
enc_flag
vagrant@ubuntu-jammy:~$ file enc_flag
enc_flag: ASCII text
vagrant@ubuntu-jammy:~$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyZzBOMm8yYXpZNWZRPT0nCg==
```
Esa cadena esta encriptada con base64. Cuando se le aplica una decodificación se obtiene lo siguiente:

**b\'d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2g0N2o2azY5fQ\==\'**

Se decodifica nuevamente lo que esta entre las comillas simples en base64 y se obtiene lo siguiente: 

**wpjvJAM{jhlzhy_k3jy9wa3k_h47j6k69}**

Esto ya tiene mas parecido a una bandera por lo que se dedujo que solo se le aplicaron rotaciones. Después de analizarla se realizo una rotación de 19 posiciones y se obtuvo la bandera: 

picoCTF{caesar_d3cr9pt3d_a47c6d69}
## Notas adicionales
## Referencias