## Objetivo
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)
## Pistas
1.- In collaborative projects, many users can make many changes. How can you see the changes within one file?
2.- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3.- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## Solución
Descargamos el archivo
```
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ ls
message.py
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ python 
.git/       message.py  
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ python 
.git/       message.py  
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ python 
.git/       message.py  
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ python message.py 
  File "/home/arcangel7651-picoctf/Concurso/Blame/drop-in/message.py", line 1
    print("Hello, World!"
         ^
SyntaxError: '(' was never closed
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ cat message.py 
print("Hello, World!"
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ nano message.py 
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ python message.py 
Hello, World!
arcangel7651-picoctf@webshell:~/Concurso/Blame/drop-in$ git log
```


Usamos git log y vamos hasta abjo y encontraremos el comit que se realizo con el author siendo la contraseña
```
commit 0351e0474493168ca76441c24630c17554fd09ca
Author: picoCTF{@sk_th3_1nt3rn_d2d29f22} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:01 2024 +0000

    optimize file size of prod code

```
## Notas Adicionales
## Referencias
