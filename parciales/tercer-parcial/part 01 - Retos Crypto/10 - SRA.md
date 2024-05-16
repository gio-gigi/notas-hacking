# Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.
# Pistas
(None)
# Solución
```
from Crypto.Util.number import getPrime, bytes_to_long
from string import ascii_letters, digits
from random import choice
from pwn import remote

pride = "".join(choice(ascii_letters + digits) for _ in range(16))
r = remote('saturn.picoctf.net', 60414)
gluttony = getPrime(128
greed = getPrime(128)
lust = gluttony * greed
sloth = 65537
r.recvuntil("anger =")
ciphertext=int(r.recvline())
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print(f"{pride = }")
pride_num = bytes_to_long(pride.encode())
print(f"El valor de vainglory es: {pride_num}")
r.sendline(str(pride_num))
response = r.recvline().strip()
# Comparamos la adivinanza del usuario con el valor real
if b"Congrats!" in response:
    print("¡Congrats!")
    with open("/challenge/flag.txt") as f:
        print(f.read())
else:
    print("Hubris")
```


```
picoCTF{7h053_51n5_4r3_n0_m0r3_dd808298}
```
# Notas adicionales
# Referencias