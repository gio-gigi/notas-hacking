# Objetivo
We found this [file](https://mercury.picoctf.net/static/21c07c9dd20cd9f2459a0ae75d99af6e/tunn3l_v1s10n). Recover the flag.
# Pistas
1. Weird that it won't display right...
# Solución
1. Se modifica el encabezado con 28 00
2. Abrimos imagen, pero aun no se muestra por el ancho.
```
┌──(gio㉿kali)-[~/picoctf/forensic/tunnelvision]
└─$ exiftool tunn3l_v1s10n  
ExifTool Version Number         : 12.67
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2024:03:21 12:43:45-06:00
File Access Date/Time           : 2024:03:21 12:43:50-06:00
File Inode Change Date/Time     : 2024:03:21 12:43:45-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
```
3. Volvemos abri el hexeditor para ajustar el tamaño de la imagen.
4. Revisamos si el tamaño concuerda y abrimos imagen.
```
──(gio㉿kali)-[~/picoctf/forensic/tunnelvision]
└─$ exiftool tunn3l_v1s10n  
ExifTool Version Number         : 12.67
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2024:03:21 12:43:45-06:00
File Access Date/Time           : 2024:03:21 12:43:50-06:00
File Inode Change Date/Time     : 2024:03:21 12:43:45-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
┌──(gio㉿kali)-[~/picoctf/forensic/tunnelvision]
└─$ open tunn3l_v1s10n  
```
5. Nos muestra la bandera en la imagen.
```
picoCTF{qu1t3_a_v13w_2020}
```
# Notas adicionales
- Magic bytes
# Referencias