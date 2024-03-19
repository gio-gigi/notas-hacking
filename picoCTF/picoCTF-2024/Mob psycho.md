# Objetivo
Can you handle APKs?Download the android apk [here](https://artifacts.picoctf.net/c_titan/140/mobpsycho.apk).
# Pistas
1. Did you know you can `unzip` APK files?
2. Now you have the whole host of shell tools for searching these files.
# Solución
1. Descargar el archivo apk.
```
wget https://artifacts.picoctf.net/c_titan/140/mobpsycho.apk
```
2. Ver algunas de sus características
```
exiftool mobpsycho.apk
exiftool mobpsycho.apk
ExifTool Version Number         : 12.67
File Name                       : mobpsycho.apk
Directory                       : .
File Size                       : 4.1 MB
File Modification Date/Time     : 2024:03:11 18:36:50-06:00
File Access Date/Time           : 2024:03:18 20:09:52-06:00
File Inode Change Date/Time     : 2024:03:18 20:09:22-06:00
File Permissions                : -rw-r--r--
File Type                       : ZIP
File Type Extension             : zip
MIME Type                       : application/zip
Zip Required Version            : 10
Zip Bit Flag                    : 0
Zip Compression                 : None
Zip Modify Date                 : 2024:03:12 00:06:28
Zip CRC                         : 0x00000000
Zip Compressed Size             : 0
Zip Uncompressed Size           : 0
Zip File Name                   : res/
Warning                         : [minor] Use the Duplicates option to extract tags for all 772 files
```
3. Nos dice que es un archivo .zip, asi que lo descomprimimos:
```
unzip mobpsycho.apk
```
4. Abrimos todos los archivos para poder darnos una idea.
5. Como son bastantes archivos, busque entre las imágenes que tiene este archivo, pero sin exito.
6. Buscar archivos con .txt en todos los archivos disponibles
```
find -type f -name "*.txt"
./res/color/flag.txt
```
7. Abrimos el archivo flag.txt
```
7069636f4354467b6178386d433052553676655f4e5838356c346178386d436c5f35653637656135657d
```
8. Es hexadecimal, asi que se realiza una conversión de hexadecimal a ASCII:
```
picoCTF{ax8mC0RU6ve_NX85l4ax8mCl_5e67ea5e}
```

# Notas adicionales
- find: Buscar archivos por nombre, tipo, tamaño, fecha etc.
# Referencias
- https://www.chileoffshore.com/es/toolkits/basic-conversion/hexa-to-ascii