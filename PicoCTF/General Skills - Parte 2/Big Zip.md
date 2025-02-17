### Description
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)
#### hint
- Can grep be instructed to look at every file in a directory and its subdirectories?





## Solución
mediante los comandos wget, unzip para extraer los archivos y grep -r para buscar la bandera

````
wget https://artifacts.picoctf.net/c/505/big-zip-files.zip
...
...
...

Gurihacker-picoctf@webshell:~$ grep -r "picoCTF"
README.txt:Welcome to the picoCTF webshell!
README.txt:picoCTF challenges.
README.txt:  Extensive brute-forcing is not necessary to solve picoCTF challenges.
README.txt:- If you change your username through the picoCTF website, you will
flag:picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}


```


