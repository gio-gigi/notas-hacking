
# Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
# Datos de acceso al nivel
username = bandit18
password = hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
# Solución
```
C:\Users\esmee>ssh bandit18@bandit.labs.overthewire.org -p2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
# Notas adicionales
Dentro del ssh nos permite hacer cat.
# Referencias