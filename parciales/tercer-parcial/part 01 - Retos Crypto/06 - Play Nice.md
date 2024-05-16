# Objetivo
Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 40742` [playfair.py](https://mercury.picoctf.net/static/283dcc58048f3a6ac83b4c11ec696954/playfair.py)
# Pistas
(None)
# Solución
```
Desarrollar dos metodos opuestos a encrypt_pair y encript_string
def decrypt_pair(pair, matrix):

    p1 = get_index(pair[0], matrix)

    p2 = get_index(pair[1], matrix)

  

    if p1[0] == p2[0]:

        return matrix[p1[0]][(p1[1] - 1) % SQUARE_SIZE] + matrix[p2[0]][(p2[1] - 1) % SQUARE_SIZE]

    elif p1[1] == p2[1]:

        return matrix[(p1[0] - 1) % SQUARE_SIZE][p1[1]] + matrix[(p2[0] - 1) % SQUARE_SIZE][p2[1]]

    else:

        return matrix[p1[0]][p2[1]] + matrix[p2[0]][p1[1]]

  

def decrypt_string(s, matrix):

    result = ""

    for i in range(0, len(s), 2):

        result += decrypt_pair(s[i:i + 2], matrix)

    return result

  

alphabet = open("key").read().rstrip()
m = generate_square(alphabet)
print(m)
msg = open("msg").read().rstrip()
enc_msg = "h5a1sqeusdi38obzy0j5h3ift7s2r2"
print(enc_msg)
plain_msg = decrypt_string(enc_msg, m)
Esta seria nuestra matriz generada:
['i', 'r', 'l', 'g', 'e', 'k'] 
['t', 'q', '8', 'a', 'y', 'f'] 
['p', '5', 'z', 'u', '0', '3'] 
['7', 'n', 'o', 'v', '1', 'm']
['9', 'x', 'b', 'c', '6', '4']
['s', 'h', 'w', 'j', 'd', '2']
┌──(gio㉿kali)-[~/tercerparcial/playnice]
└─$ nc mercury.picoctf.net 40742
Here is the alphabet: irlgektq8ayfp5zu037nov1m9xbc64shwjd2
Here is the encrypted message: h5a1sqeusdi38obzy0j5h3ift7s2r2
What is the plaintext message? xqyvhtg02jkplzo8eyhu25ktip2dkh
Congratulations! Here's the flag: 25a0ea7ff711f17bddefe26a6354b2f3
```

```
25a0ea7ff711f17bddefe26a6354b2f3
```
# Notas adicionales
# Referencias
- https://en.wikipedia.org/wiki/Playfair_cipher