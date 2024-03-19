# Objetivo
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/13/challenge.zip)

Additional details will be available after launching your challenge instance.

The same files are accessible via SSH here:`ssh -p 52290 ctf-player@atlas.picoctf.net`Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
# Pistas
1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text
# Solución
1. Nos conectamos al ssh:
```
giogi-picoctf@webshell:~$ cd sacnsurprise
giogi-picoctf@webshell:~/sacnsurprise$ ssh -p 58409 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:58409 ([18.217.83.136]:58409)' can't be established.
ED25519 key fingerprint is SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:58409' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
```
2. En este caso se cuenta con un dispositivo con ios 17, asi que solo se escanea el código QR que nos muestra la conexión.

![[Imagen de WhatsApp 2024-03-15 a las 16.46.17_ed3eaef9.jpg]]
3. Se escanea y nos da la bandera:
```
picoCTF{p33k_@_b00_d4ca652e}
```
5. Se cierra conexión:
```
ctf-player@challenge:~/drop-in$ Connection to atlas.picoctf.net closed by remote host.
Connection to atlas.picoctf.net closed.
```
# Notas adicionales
- Es posible obtener información mediante el escaneo de códigos QR.
# Referencias