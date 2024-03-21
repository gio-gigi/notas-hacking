# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
# Pistas
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
# Solución
Primera solución:
1. Descargar archivos.
2. Usamos wireshark.
3. Editar/Preferencias/Protocolos y buscamos el TCP, ahi agregamos la llave.
4. Seleccionamos aquel que tenga HTTP, segumos y solo buscamos la palabra picoCTF.
```
picoCTF{nongshim.shrimp.crackers}
```
Segunda solución:
```
┌──(gio㉿kali)-[~/picoctf/forensic/webnet0]
└─$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A3
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
    65 6e 67 74 68 3a 20 38 32 31 0d 0a 4b 65 65 70    ength: 821..Keep
```
# Notas adicionales
# Referencias