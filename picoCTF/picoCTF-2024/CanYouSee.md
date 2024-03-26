# Objetivo
How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/128/unknown.zip).
# Pistas
1. How can you view the information about the picture?
2. If something isn't in the expected form, maybe it deserves attention?
# Solución
1. Se descarga el archivo para realizar el reto.
2. Descomprimir el archivo .zip
```
unzip unknown.zip
```
3.  Abrimos la imagen, pero no se visualiza el picoCTF.
4. Hacemos uso de exiftool.
```
┌──(gio㉿kali)-[~/picoctf/picoctf2024/canyousee]
└─$ exiftool ukn_reality.jpg        
ExifTool Version Number         : 12.67
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 18:05:51-06:00
File Access Date/Time           : 2024:03:26 09:30:30-06:00
File Inode Change Date/Time     : 2024:03:26 09:30:30-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fM2I5MjA5YTJ9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4

```
5. Identificamos Attrivution URL que esta en base64
```
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fM2I5MjA5YTJ9Cg==

picoCTF{ME74D47A_HIDD3N_3b9209a2}
```


# Notas adicionales
# Referencias
- https://www.base64decode.org/