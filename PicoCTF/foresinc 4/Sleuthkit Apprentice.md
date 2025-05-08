### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)

#### hint
-(None)
# Solución 
descargamos nuestro archivo y lo extraemos una vez ahí obtenemos el archivo usamos mmls para obtener información y donde inicia nuestro particion usamos un fls para ver el contenido, vemos un archivo flag así que usaremos un icat
```
guri@LAPTOP-05MLJNS4:~/Fundamentos/aprendiz$ ls -lah disk.flag.img
-rw-r--r-- 1 guri guri 300M Mar 15  2023 disk.flag.img
guri@LAPTOP-05MLJNS4:~/Fundamentos/aprendiz$ mmls  disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
guri@LAPTOP-05MLJNS4:~/Fundamentos/aprendiz$ fls disk.flag.img -o 360448 -r

guri@LAPTOP-05MLJNS4:~/Fundamentos/aprendiz$ icat disk.flag.img -o 360448 2371
picoCTF{by73_5urf3r_2f22df38}


```

