# Objetivo
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.You can download the challenge files here:

- `[challenge.zip](https://artifacts.picoctf.net/c_rhea/20/challenge.zip)`

The same files are accessible via SSH here:`ssh -p 62557 ctf-player@rhea.picoctf.net`Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

- Checksum: fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7
- To decrypt the file once you've verified the hash, run `./decrypt.sh files/<file>`.
# Pistas
1. Checksums let you tell if a file is complete and from the original distributor. If the hash doesn't match, it's a different file.
2. You can create a SHA checksum of a file with `sha256sum <file>` or all files in a directory with `sha256sum <directory>/*`.
3. Remember you can pipe the output of one command to another with `|`. Try practicing with the 'First Grep' challenge if you're stuck!
# Solución
1. Nos conectamos al ssh:
`ssh -p 62557 ctf-player@rhea.picoctf.net`
2. Verificamos el contenido dentro.
```
ctf-player@pico-chall$ ls
checksum.txt  decrypt.sh  files
```
3.  Probamos la pista número 2, y nos damos cuenta que el archivo txt es una bandera falsa.
```
ctf-player@pico-chall$ sha256sum checksum.txt
da498696036e38f06e75a154878b42a28e14701405140a71f1f5a1e147e071d1  checksum.txt
```
4. Abrimos los archivos que nos muestran, y decrypt.sh se muestra un código que si le dan el archivo que tiene la llave correcta nos muestra la bandera. Ejecutamos el script con el archivo txt que tiene al inicio.
```
ctf-player@pico-chall$ ./decrypt.sh checksum.txt
bad magic number
Error: Failed to decrypt 'checksum.txt'. This flag is fake! Keep looking!
```
5. Buscamos entre los archivos un archivo que sea idéntico al Checksum. Que nos muestre el valor hash pero haciendo uso de grep para que sea buscar el checksum que se nos dio al principio.
```
ctf-player@pico-chall$ sha256sum files/* | grep fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7
fba9f49bf22aa7188a155768ab0dfdc1f9b86c47976cd0f7c9003af2e20598f7  files/87590c24
```
6. Ejecutamos el script con la ruta y nombre del archivo donde se encuentra el Checksum:
```
ctf-player@pico-chall$ ./decrypt.sh files/87590c24
picoCTF{trust_but_verify_87590c24}
```
# Notas adicionales
- sha256sum: Nos muestra el valor hash SHA-256 de un archivo.
# Referencias