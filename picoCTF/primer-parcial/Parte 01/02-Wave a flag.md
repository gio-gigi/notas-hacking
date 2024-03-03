# Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm) has extraordinarily helpful information...
# Pistas
1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4. -h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.
# Solución
```
giogi-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
--2024-02-27 18:23:53--  https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm.1'

warm.1                       100%[=============================================>]  10.68K  --.-KB/s    in 0s      

2024-02-27 18:23:53 (225 MB/s) - 'warm.1' saved [10936/10936]

giogi-picoctf@webshell:~$ ls
README.txt  flag  warm  warm.1
giogi-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
giogi-picoctf@webshell:~$ rv warm.1
-bash: rv: command not found
giogi-picoctf@webshell:~$ rm warm.1
giogi-picoctf@webshell:~$ ls
README.txt  flag  warm
giogi-picoctf@webshell:~$ chmod +x warm
giogi-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
giogi-picoctf@webshell:~$ -h
-bash: -h: command not found
giogi-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
# Notas adicionales
chmod: permite cambiar los permisos de un archivo.
# Referencias
