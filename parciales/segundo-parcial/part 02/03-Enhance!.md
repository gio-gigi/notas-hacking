# Objetivo
Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/102/drawing.flag.svg)
# Pistas
# Solución
```
┌──(gio㉿kali)-[~/picoctf/forensic/enhance]
└─$ strings drawing.flag.svg | grep pico
                                                                                                      
┌──(gio㉿kali)-[~/picoctf/forensic/enhance]
└─$ strings drawing.flag.svg            
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!-- Created with Inkscape (http://www.inkscape.org/) -->
<svg
┌──(gio㉿kali)-[~/picoctf/forensic/enhance]
└─$ strings drawing.flag.svg | grep "</tspan>"
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ d 0 a 7 5 7 b f }</tspan></text>
```
picoCTF{3nh4ncd_d0a757bf}
# Notas adicionales
# Referencias