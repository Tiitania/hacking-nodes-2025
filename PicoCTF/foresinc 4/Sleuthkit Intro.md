### Description

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.

#### hint
- Look at the problem category
# Solución 
descargamos nuestro archivo y lo extraemos una vez ahí obtenemos el archivo usamos mmls para obtener información
```
guri@LAPTOP-05MLJNS4:~/Fundamentos$ ls -lah disk.img
-rw-r--r-- 1 guri guri 100M Aug  4  2023 disk.img
guri@LAPTOP-05MLJNS4:~/Fundamentos$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

ahora ejecutamos el launcher e ingresamos a la instancia
guri@LAPTOP-05MLJNS4:~$ nc saturn.picoctf.net 49303
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}


```

