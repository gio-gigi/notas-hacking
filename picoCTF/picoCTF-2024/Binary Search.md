## Objetivo
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/17/challenge.zip)

`ssh -p 50388 ctf-player@atlas.picoctf.net` Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Pistas
### 1
Have you ever played hot or cold? Binary search is a bit like that.
### 2
You have a very limited number of guesses. Try larger jumps between numbers!
### 3
The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solución
```
┌──(rio11㉿kali)-[~/Documents]
└─$ ssh -p 50388 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:50388 ([18.217.83.136]:50388)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[atlas.picoctf.net]:50388' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 875
Lower! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 775
Lower! Try again.
Enter your guess: 760
Higher! Try again.
Enter your guess: 770
Lower! Try again.
Enter your guess: 765
Higher! Try again.
Enter your guess: 767
Lower! Try again.
Enter your guess: 766
Congratulations! You guessed the correct number: 766
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
                                                                                                                                                                       
┌──(rio11㉿kali)-[~/Documents]
└─$ 
```
## Bandera Obtenida
picoCTF{g00d_gu355_6dcfb67c}
## Notas adicionales
Aquí utilizamos el algoritmo de la busqueda binario o divide y venceras 
## Referencias