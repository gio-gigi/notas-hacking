# Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.
# Pistas
1. objdump and Gihdra are some tools that could assist with this
# Solución
```
sudo apt install ghidra
┌──(gio㉿kali)-[~/picoctf/reversing/reversecipher]
└─$ cat rev_this 
picoCTF{w1{1wq85jc=2i0<}                                                                             

Script exp.py
d = open("rev_this").read()
flag = ""
for j in range(0,23):
        if j & 1 == 0:
                flag += chr( ord(d[j]) - 5)
        else:
                flag += chr( ord(d[j]) + 2)

print(flag)

㉿kali)-[~/picoctf/reversing/reversecipher]
└─$ python exp.py
r3v3rs37ee84d27
                           

```
s
```
picoCTF{r3v3rs37ee84d27}
```
# Notas adicionales
# Referencias