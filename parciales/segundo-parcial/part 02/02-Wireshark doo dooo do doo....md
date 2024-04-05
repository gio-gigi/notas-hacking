# Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/4c996ecfb7fbada15a9799511f24dc99/shark1.pcapng).
# Pistas
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/wiresharkdoo]
└─$ ls
shark1.pcapng
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/wiresharkdoo]
└─$ wireshark shark1.pcapng
```
1. tcp.stream eq 5
```
HTTP/1.1 200 OK
Date: Mon, 10 Aug 2020 01:51:45 GMT
Server: Apache/2.4.29 (Ubuntu)
Last-Modified: Fri, 07 Aug 2020 00:45:02 GMT
ETag: "2f-5ac3eea4fcf01"
Accept-Ranges: bytes
Content-Length: 47
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html

Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
```
2. ROT13
```
picoCTF{p33kab00_1_s33_u_deadbeef}
```
# Notas adicionales
# Referencias
- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tjMzN4bm8wMF8xX2YzM19oX3FybnFvcnJzfQ