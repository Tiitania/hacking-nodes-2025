### Most Cookies
### Description 

Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/cae5577e6b8f86e17d7884723204f61e/server.py) [http://mercury.picoctf.net:6259/](http://mercury.picoctf.net:6259/)
### Hint

- Have you heard of JWT?
- What is that cookie?

## Solución  1
```
Nos registramos y con el intercept burp, rellenamos los datos
-le damos a forward
-en 2 fa authentication ponermo la misma contraseña
-le damos en submit
-con el intercept burp eliminamos la otp completa
-le damos foward y obtenemos la bandera
Welcome, guri you sucessfully bypassed the OTP request. Your Flag: 
picoCTF{#0TP_Bypvss_SuCc3$S_c94b61ac}

```