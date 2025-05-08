### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)

#### hint
- (None)
# Solución 

```
guri@LAPTOP-05MLJNS4:~/Fundamentos$ fls  disk.flag.img -o 411648 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
guri@LAPTOP-05MLJNS4:~/Fundamentos$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567

picoCTF{h4un71ng_p457_5113beab}
```

