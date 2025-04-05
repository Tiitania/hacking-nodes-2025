### Most Cookies
### Description 

Can you get the flag?Go to this [website](http://saturn.picoctf.net:64252/) and see what you can discover.
### Hint

- How is the password checked on this website?

## Solución  1
```
  investigamos en el inspeccionar y depues vemos la fuente de codigo
  dentro del saurce.js y encontramos el user y el password, eso lo sabemos ya que el script del javascript nos muestra el filtro para la contraseña
  
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

intresamos los datos correctos y obtenemos la bandera
  
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}


```