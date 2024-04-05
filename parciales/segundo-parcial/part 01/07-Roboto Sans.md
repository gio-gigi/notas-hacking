# Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:59901/) out.
# Pistas
# Solución
1. robots.txt
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```
2. Decodificamos cada lineal por separado (base64), dandonos la ruta /js/myfile.txt
```
picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
```
# Notas adicionales
# Referencias