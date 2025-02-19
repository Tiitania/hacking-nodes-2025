## Codebook

### Description 
Run the Python script `code.py` in the same directory as `codebook.txt`.

### Hint
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
hay que tener los 2 archivos en el mismo directorio
```
Gurihacker-picoctf@webshell:~$ 
Gurihacker-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
Gurihacker-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
Gurihacker-picoctf@webshell:~$ ls
Addadshashanammu  README.txt  big-zip-files  code.py  codebook.txt  files
Gurihacker-picoctf@webshell:~$ 
Gurihacker-picoctf@webshell:~$ python code.py
picoCTF{c0d3b00k_455157_7d102d7a}
```

