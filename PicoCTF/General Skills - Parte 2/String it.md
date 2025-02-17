## String it
### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?```
#### hint
- [strings](https://linux.die.net/man/1/strings)

## Solución
mediante el uso de strings para ver las cadenas, y ya buscamos nuestro objetivo mediante grep
 ```
chmod +x strings

 Gurihacker-picoctf@webshell:~$ strings -n 10 strings | grep pico
picoCTF{5tRIng5_1T_827aee91}
``` 

