# Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
# Pistas
1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.
# Solución
```
giogi-picoctf@webshell:~/0304$ python level2.py
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/giogi-picoctf/0304/level2.py", line 27, in <module>
    level_2_pw_check()
  File "/home/giogi-picoctf/0304/level2.py", line 17, in level_2_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

giogi-picoctf@webshell:~/0304$ nano level2.py
giogi-picoctf@webshell:~/0304$ python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```
# Notas adicionales
# Referencias