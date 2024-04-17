# Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)
# Pistas
1. Bits are expensive, I used only a little bit over 100 to save money
# Solución
```
giogi-picoctf@webshell:~/crypto$ python3
Python 3.10.12 (main, Nov 20 2023, 15:14:05) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> exit()
giogi-picoctf@webshell:~/crypto$ cat values
Decrypt my super sick RSA:
c: 421345306292040663864066688931456845278496274597031632020995583473619804626233684
n: 631371953793368771804570727896887140714495090919073481680274581226742748040342637
e: 65537giogi-picoctf@webshell:~/crypto$ python3
Python 3.10.12 (main, Nov 20 2023, 15:14:05) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> p = 1461849912200000206276283741896701133693
>>> q = 431899300006243611356963607089521499045809
>>> p*q
631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> n = p*q
>>> tn = (p-1)*(q-1)
>>> e = 65537
>>> d = pow(e,-1,tn)
>>> c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
>>> m = pow(c, d, n)
>>> bytes.fromhex( hex(m)[2:] )
b'picoCTF{sma11_N_n0_g0od_55304594}'
```
# Notas adicionales
e = 65537
# Referencias
- http://factordb.com/index.php?query=631371953793368771804570727896887140714495090919073481680274581226742748040342637