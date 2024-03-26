# Objetivo
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf).
# Pistas
1. This problem can be solved by just opening the file in different ways
# Solución
1. Descargamos el archivo
```
┌──(gio㉿kali)-[~/picoctf/picoctf2024/secretofthepolyglot]
└─$ wget https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf
--2024-03-15 18:16:07--  https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.107, 18.154.144.103, 18.154.144.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.107|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf  100%[================>]   3.28K  --.-KB/s    in 0s      

2024-03-15 18:16:08 (23.3 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]
```
2. Abrimos el archivo pdf:
```
open flag2of2-final.pdf
```
Adentro de este pdf encontraremos una parte de CTF *1n_pn9_&_pdf_90974127}*

3.  Cambiamos la extensión del pdf a png:
```
 mv flag2of2-final.pdf flag2of2-final.png
```
4. Abrimos la imagen:
```
open flag2of2-final.png
```
La imagen contiene el principio de CTF: *picoCTF{f1u3n7_*
5. Unimos ambas partes y nos da la siguiente bandera:
```
->  picoCTF{f1u3n7_1n_pn9_&_pdf_90974127}
```
# Notas adicionales
# Referencias