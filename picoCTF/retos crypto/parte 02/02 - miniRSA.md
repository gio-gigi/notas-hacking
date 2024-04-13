# Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.
# Pistas
1. RSA [tutorial](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
2. How could having too small an e affect the security of this 2048 bit key?
3. Make sure you don't lose precision, the numbers are pretty big (besides the e value)
# Solución
```
c = 2205316413931134031074603746928247799030155221252519872650073010782049179856976080512716237308882294226369300412719995904064931819531456392957957122459640736424089744772221933500860936331459280832211445548332429338572369823704784625368933 
def find_cubic_root(n):
    a = 1
    b = n
    while b - a > 1:
        mid = (a + b) // 2
        if mid**3 > n:
            b = mid
        else:
            a = mid

    if a ** 3 == n:
        return a
    elif b ** 3 == n:
        return b
    else:
        return 0

m = find_cubic_root(c)
h = hex(m)
print(h)
p = bytes.fromhex(hex(m)[2:])
print(p)

```

```
┌──(gio㉿kali)-[~/picoctf/criptografia/miniRSA]
└─$ python rsa.py -e 3 -n TODO --uncipher
0x7069636f4354467b6e3333645f615f6c41726733725f655f63636161373737367d
b'picoCTF{n33d_a_lArg3r_e_ccaa7776}'
```
# Notas adicionales
$$
m = 3 raiz c
$$
# Referencias