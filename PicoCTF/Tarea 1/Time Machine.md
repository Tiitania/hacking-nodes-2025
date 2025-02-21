## Time Machine
### Description 

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/163/challenge.zip)
### Hint

- The `cat` command will let you read a file, but that won't help you here!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- When committing a file with git, a message can (and should) be included.

## Solución 
```
Gurihacker-picoctf@webshell:~/drop-in/drop-in/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...

Gurihacker-picoctf@webshell:~/drop-in/drop-in/drop-in$ git checkout message.txt
Updated 1 path from the index

Gurihacker-picoctf@webshell:~/drop-in/drop-in/drop-in$ git log
commit e65fedb3a72a16c577f4b17023b63997134b307d (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:29 2024 +0000

    picoCTF{t1m3m@ch1n3_88c35e3b}

```
