# Objetivo
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics%20is%20fun.pptm)
# Pistas
# Solución
1. Se descarga el archivo.
2. Se descomprime el archivo .pptm
```
┌──(gio㉿kali)-[~/picoctf/forensic/macrohardweakedge]
└─$ unzip Forensics\ is\ fun.pptm 
....
....
inflating: ppt/slideMasters/hidden 
```
Primera solución:
```
──(gio㉿kali)-[~/picoctf/forensic/macrohardweakedge]
└─$ cd ppt/slideMasters/      
                                                                                 
┌──(gio㉿kali)-[~/…/forensic/macrohardweakedge/ppt/slideMasters]
└─$ ls    
_rels  hidden  slideMaster1.xml
                                                                                 
┌──(gio㉿kali)-[~/…/forensic/macrohardweakedge/ppt/slideMasters]
└─$ cat hidden 
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                         ```
```
Segunda solución:
```
──(gio㉿kali)-[~/…/forensic/macrohardweakedge/ppt/slideMasters]
└─$ cat hidden | tr -d ' ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
                                                              
```
# Notas adicionales
- Extension m: Puede ser peligroso, o sea que son macros.
# Referencias