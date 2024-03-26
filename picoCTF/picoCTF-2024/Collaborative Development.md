## Objetivo
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)
## Pistas
1.- `git branch -a` will let you see available branchesç
2.- How can file 'diffs' be brought to the main branch? Don't forget to git config!
## Solución
```
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment$ ls
challenge.zip  drop-in
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment$ git branch -a 
fatal: not a git repository (or any parent up to mount point /)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment$ cd drop-in/
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git branch -a 

[5]+  Stopped                 git branch -a
```
Observamos las ramas que tenemos
```
  feature/part-1
  feature/part-2
  feature/part-3
* main
(END)
```

Las fucionamos
```
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment$ ls
challenge.zip  drop-in
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment$ cd drop-in/
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git branch -a

[9]+  Stopped                 git branch -a
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git merge feature/part-1
Updating eb19d0e..0cd57e0
Fast-forward
 flag.py | 1 +
 1 file changed, 1 insertion(+)
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git merge feature/part-2
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
```
Observamos que hay en nuestro archivo
```
print("Printing the flag...")
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2

```
Modificamos para borrar los comentarios de git
y despues fucionamos con la tercera parte y hacemos un commit
```
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git add flag.py 
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git commit
[feature/nueva ef7141a] Merge branch 'feature/part-2' into feature/nueva
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ git merge feature/part-3
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ cat flag.py 
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
print("m@k3s_th3_dr3@m_", end='')

=======
print("Printing the flag...")

print("w0rk_2c91ca76}")
>>>>>>> feature/part-3
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ nano flag.py 
arcangel7651-picoctf@webshell:~/Concurso/collab_deplyment/drop-in$ python flag.py 
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}
```

## Notas Adicionales
## Referencias
https://www.atlassian.com/es/git/tutorials/using-branches/git-merge
