# Objetivo
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704
# Pistas
1. You don't need to download a new web browser
# Solución
```
giogi-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/26704/flag -H "User-Agent: picobrowser" | grep pico
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2115  100  2115    0     0   7277      0 --:--:-- --:--:-- --:--:--  7293
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}</code></p>
```
# Notas adicionales
# Referencias