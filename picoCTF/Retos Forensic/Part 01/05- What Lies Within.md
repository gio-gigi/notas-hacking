# Objetivo
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
# Pistas
1. There is data encoded somewhere... there might be an online decoder.
# Solución
![[Imagen de WhatsApp 2024-03-12 a las 12.55.53_d292efc5.jpg]]
```
picoCTF{h1d1ng_1n_th3_b1t5}
┌──(gio㉿kali)-[~/picoctf/forensic/whatlieswithin]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
```
# Notas adicionales
- esteganografia
# Referencias
