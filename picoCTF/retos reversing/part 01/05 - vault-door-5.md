# Objetivo
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/0a53bf0deaba6919f98d8550c35aa253/VaultDoor5.java)
# Pistas
1. You may find an encoder/decoder tool helpful, such as https://encoding.tools/
2. Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.
# Solución
```
From base64
URL Decode
JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVmJTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTMwJTYyJTM5JTM1JTM3JTYzJTM0JTY2
Bandera:
picoCTF{c0nv3rt1ng_fr0m_ba5e_64_0b957c4f}
```
# Notas adicionales
- Código porciento: se usa para escribir identificadores de nombres y ubicaciones URL.
	- Por ejemplo %28 es un "("
# Referencias
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm1KVFkySlRjeUpUTXdKVFprSlRWbUpUWXlKVFl4SlRNMUpUWTFKVFZtSlRNMkpUTTBKVFZtSlRNd0pUWXlKVE01SlRNMUpUTTNKVFl6SlRNMEpUWTI&ieol=CRLF