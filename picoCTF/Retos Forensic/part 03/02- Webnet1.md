# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
# Pistas
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
# Solución
1. Descargamos archivos usando el comando wget.
2. Extraemos el listado de objetos HTTP.
3. Eligimos la imagen y guardamos.
```
──(gio㉿kali)-[~/picoctf/forensic/webnet1]
└─$ strings -n 10 vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}

Segunda solución:
┌──(gio㉿kali)-[~/picoctf/forensic/webnet1]
└─$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A3             
    61 67 3a 20 70 69 63 6f 43 54 46 7b 74 68 69 73    ag: picoCTF{this
    2e 69 73 2e 6e 6f 74 2e 79 6f 75 72 2e 66 6c 61    .is.not.your.fla
    67 2e 61 6e 79 6d 6f 72 65 7d 0d 0a 43 6f 6e 74    g.anymore}..Cont
    65 6e 74 2d 4c 65 6e 67 74 68 3a 20 38 34 37 0d    ent-Length: 847.

```
# Notas adicionales
# Referencias