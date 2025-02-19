## PW Crack 2 

### Description 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

### Hint
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
al abrir el codigo con el comando nano nos  muestra en hexa el user, por lo que tendremos que usar cyberchef

````
input:chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) 

recipe: From Hex

output: de76
```

```
Gurihacker-picoctf@webshell:~$ nano level2.py
Gurihacker-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}