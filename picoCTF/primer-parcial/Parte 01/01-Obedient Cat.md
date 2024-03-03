# Objetivo
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).

# Pistas
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag`
3. $ man cat
# Solución
```
giogi-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
--2024-02-27 18:32:04--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag.1'

flag.1                       100%[=============================================>]      34  --.-KB/s    in 0s      

2024-02-27 18:32:04 (14.3 MB/s) - 'flag.1' saved [34/34]

giogi-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
```
# Notas adicionales
- wget : permite descargar archivos a la terminal.
# Referencias