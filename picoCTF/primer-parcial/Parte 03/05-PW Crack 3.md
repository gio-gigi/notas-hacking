# Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

# Pistas
1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
2. To exit `bvi` type `:q` and press enter.
3. The `str_xor` function does not need to be reverse engineered for this challenge.
# Solución
```
iogi-picoctf@webshell:~/level3$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
giogi-picoctf@webshell:~/level3$ nano level3.py
giogi-picoctf@webshell:~/level3$ python level3.py
Please enter correct password for flag: 
That password is incorrect
Correct password found: 2295
Flag: picoCTF{m45h_fl1ng1ng_6f98a49f}
```
# Notas adicionales
# Referencias