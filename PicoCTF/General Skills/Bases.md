## Bases

### Description 
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

### Hint
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solución 1
mediante la base 64 con la libreria de python
]```
```
import base64

Decodificaciom = base64.b64decode("bDNhcm5fdGgzX3IwcDM1")

print(Decodificaciom)

PS D:\python> & C:/Users/pando/AppData/Local/Programs/Python/Python313/python.exe d:/python/2warm.py
b'l3arn_th3_r0p35'

PicoCTF{l3arn_th3_r0p35}
```

# Solución 2
resolver con cyberchef
```
Input: bDNhcm5fdGgzX3IwcDM1

Recipe:From Base64

Output: l3arn_th3_r0p35
```


### Referencias
- https://gchq.github.io/CyberChef/
