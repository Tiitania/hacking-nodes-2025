### More SQLi
### Description 

There is some interesting information hidden around this site [http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/). Can you find it?
### Hint

-  You should have enough hints to find the files, don't run a brute forcer.

## Solución  1
```
import jwt
payload = {"user": "admin"}
# Secreto para firmar el token
secret = "ilovepico"
token = jwt.encode(payload, secret, algorithm="HS256")
print("Token JWT firmado:", token)
```