### GET aHEAD
### Description 

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)
### Hint

- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses

## Solución  1
```
utilizamos el comando curl -I para obtener los encabezados de http de la url. Se suele usar para verificar el estado de un sitio web

octaviio@LAPTOP-05MLJNS4:~$ curl -I http://mercury.picoctf.net:28916/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
Content-type: text/html; charset=UTF-8

```