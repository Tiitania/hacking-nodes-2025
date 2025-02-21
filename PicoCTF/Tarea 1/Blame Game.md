## Blame Game
### Description 

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)
### Hint

- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.

## Solución  1
extraemos el archivo y dentro usamos el comando grep
```
Gurihacker-picoctf@webshell:~/drop-in$ grep -r picoCTF{
.git/logs/HEAD:2dd46769e2d65656bb14aed0ff5d3237daaa7d9d fadeca9476b6713ec8cdda633aca9e9aebffc698 picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com> 1710018551 +0000    commit: optimize file size of prod code
.git/logs/refs/heads/master:2dd46769e2d65656bb14aed0ff5d3237daaa7d9d fadeca9476b6713ec8cdda633aca9e9aebffc698 picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com> 1710018551 +0000       commit: optimize file size of prod code

```
## Solución 2
usamos el comando git log. git log muestra las instantáneas confirmadas
````
Gurihacker-picoctf@webshell:~/drop-in$ git log message.py

commit fadeca9476b6713ec8cdda633aca9e9aebffc698
Author: picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com>
Date:   Sat Mar 9 21:09:11 2024 +0000

    optimize file size of prod code

commit 2dd46769e2d65656bb14aed0ff5d3237daaa7d9d
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:11 2024 +0000

    create top secret project
```