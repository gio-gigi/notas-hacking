# Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
# Pistas
1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.
# Solución
```
giogi-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2024-03-03 21:53:01--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                    100%[============================================>]     837  --.-KB/s    in 0s      

2024-03-03 21:53:01 (40.8 MB/s) - 'fixme1.py' saved [837/837]

giogi-picoctf@webshell:~$ python fixme1.py
  File "/home/giogi-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
giogi-picoctf@webshell:~$ nano fixme1.py
giogi-picoctf@webshell:~$ python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
# Notas adicionales
# Referencias