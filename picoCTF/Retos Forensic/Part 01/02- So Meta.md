# Objetivo
Find the flag in this picture.
# Pistas
1. What does meta mean in the context of files?
2. Ever heard of metadata?
# Solución
```
──(gio㉿kali)-[~/picoctf/forensic/someta]
└─$ ls
pico_img.png
                                                                             
┌──(gio㉿kali)-[~/picoctf/forensic/someta]
└─$ strings -n 10 pico_img.png | grep pico
picoCTF{s0_m3ta_fec06741}
┌──(gio㉿kali)-[~/picoctf/forensic/someta]
└─$ exiftool pico_img.png
ExifTool Version Number         : 12.67
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2020:10:26 12:38:23-06:00
File Access Date/Time           : 2024:03:12 12:24:44-06:00
File Inode Change Date/Time     : 2024:03:12 12:23:26-06:00
File Permissions                : -rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Warning                         : [minor] Text/EXIF chunk(s) found after PNG IDAT (may be ignored by some readers)
Artist                          : picoCTF{s0_m3ta_fec06741}
Image Size                      : 600x600
Megapixels                      : 0.360
                                                                             
┌──(gio㉿kali)-[~/picoctf/forensic/someta]
└─$ exiftool pico_img.png -Artist
Artist                          : picoCTF{s0_m3ta_fec06741}

```
# Notas adicionales
- Metadatos: 
# Referencias