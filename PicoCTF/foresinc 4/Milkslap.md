### Description

[🥛](http://mercury.picoctf.net:5013/)

#### hint
- Look at the problem category
# Solución 
w

```
ubicamos en donde se encuentra la imagen,  en este caso en el css concat_v.png
Descargamos la imagen y usamos el zsteg para encontrar información escondida

Gurihacker-picoctf@webshell:~$ export RUBY_VM_STACK_SIZE=500000000
Gurihacker-picoctf@webshell:~$ zsteg -a concat_v.png 

picoCTF{imag3_m4n1pul4t10n_sl4p5}

```

