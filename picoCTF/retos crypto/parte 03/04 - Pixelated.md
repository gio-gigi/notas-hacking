# Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png)
# Pistas
1. [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
2. Think of different ways you can "stack" images
# Solución
```
┌──(gio㉿kali)-[~/picoctf/pixelated]
└─$ convert scrambled1.png scrambled2.png -compose Add -composite flag.png

                                                                             
┌──(gio㉿kali)-[~/picoctf/pixelated]
└─$ open flag.png 
```
```
picoCTF{d562333d}
```
# Notas adicionales
# Referencias
- https://en.wikipedia.org/wiki/Visual_cryptography#:~:text=Visual%20cryptography%20is%20a%20cryptographic,who%20developed%20it%20in%201994.