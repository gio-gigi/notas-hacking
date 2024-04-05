# Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:59126/) and see what you can discover.
# Pistas
1. How is the password checked on this website?
# Solución
1. Intentar ingresar algún user y password.
2. Se encontro un script secure.js:
```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}
# Notas adicionales
# Referencias