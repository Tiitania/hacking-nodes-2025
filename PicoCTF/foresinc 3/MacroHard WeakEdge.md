### Description

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm)

#### hint
- (None)
# Solución 
 Estamos navegando por directorios para encontrar un archivo llamado hidden. Luego, eliminamos los espacios del contenido con sed y lo decodificamos con base64. 

```

  inflating: ppt/slideMasters/hidden  
Gurihacker-picoctf@webshell:~$ ls
 Addadshashanammu         README.txt             _rels           challenge.zip   drop-in   ende.py   fixme1          flag.txt.en   hash   message.wav     mystery   pw.txt   whitepages.txt
'Forensics is fun.pptm'  '[Content_Types].xml'   big-zip-files   docProps        eltoken   files     fixme1.tar.gz   flaggg.png    home   message.wav.1   ppt       sstv
Gurihacker-picoctf@webshell:~$ cd macro
-bash: cd: macro: No such file or directory
Gurihacker-picoctf@webshell:~$ cd mac
-bash: cd: mac: No such file or directory
Gurihacker-picoctf@webshell:~$ cd ppt
Gurihacker-picoctf@webshell:~/ppt$  cd slideMasters/
Gurihacker-picoctf@webshell:~/ppt/slideMasters$ cat hidden 
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f QGurihacker-picoctf@webshell:~/ppt/slideMasters$ cat hidden | sed 's/ //'
Zm x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f QGurihacker-picoctf@webshell:~/ppt/slideMasters$ cat hidden | sed 's/ //g'
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQGurihacker-picoctf@webshell:~/ppt/slideMasters$ 
Gurihacker-picoctf@webshell:~/ppt/slideMasters$ cat hidden | sed 's/ //g' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
Gurihacker-picoctf@webshell:~/ppt/slideMasters$ 
```

