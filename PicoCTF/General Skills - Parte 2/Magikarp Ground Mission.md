### Description
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `b60940ca`

Additional details will be available after launching your challenge instance.
#### hint
- Finding a cheatsheet for bash would be really helpful!
## Solución
se resolvió mediante le uso de cat y de ls y cd para moverse entre los archivos


````
ctf-player@pico-chall$ 
ctf-player@pico-chall$ 
ctf-player@pico-chall$ LS
-bash: LS: command not found
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat -a 1of3.flag.txt
cat: invalid option -- 'a'
Try 'cat --help' for more information.
ctf-player@pico-chall$ cat -n 1of3.flag.txt
     1  picoCTF{xxsh_
     
2DA PARTE-----------
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
ctf-player
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat -n instructions-to-3of3.txt 
     1  Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cat -n 2of3.flag.txt
     1  0ut_0f_\/\/4t3r_




3RA PARTE-----
ctf-player@pico-chall$ cat -n instructions-to-3of3.txt 
     1  Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat -n 3of3.flag.txt
     1  c1754242}
     
picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}

```