## Static ain´t always noise
### Description

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!

#### hint
-- (None)


## Solución
Como el static es un ejecutable  entones se podía usar mediante ensablaje o un grep despues de ejecutar
```
octaviio@LAPTOP-05MLJNS4:~$ bash ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
octaviio@LAPTOP-05MLJNS4:~$ ls
PSA232  ltdis.sh    objetivo    objetivo.tct  static    static.2                  static.ltdis.x86_64.txt
SO      ltdis.shes  objetivo.c  objetivo.txt  static.1  static.ltdis.strings.txt
octaviio@LAPTOP-05MLJNS4:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_6f8c8200}prompt