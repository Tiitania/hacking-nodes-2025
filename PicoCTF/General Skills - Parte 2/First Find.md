## First Find
### Description
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
#### hint
- (NONE)

## Solución
usamos el comando grep de manera general para que nos mostrara todos nuestros archivos que contuviera una bandera, en este caso sabemos cual es nuestra bandera correcta por la hubicación en la que se encuentra nuesrto archivo en este caso uber-secret.txt
````
Gurihacker-picoctf@webshell:~$ grep -r "picoCTF{"               
flag:picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
grep: files.zip: binary file matches
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}

Bandera: picoCTF{f1nd_15_f457_ab443fd1}

```

