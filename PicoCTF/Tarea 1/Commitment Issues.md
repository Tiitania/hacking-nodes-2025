## Commitment Issues
### Description 

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)
### Hint

- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
- you can 'checkout' commits to see the files inside them

## Solución 

despues de aplicar un checkout se muesrta un .txt, en ese caso en vez de usar *cat* usamos el comando *grep*
```
Gurihacker-picoctf@webshell:~/drop-in/drop-in$ git log
Gurihacker-picoctf@webshell:~/drop-in/drop-in$ git checkout 3899edb7f3110d613c72ad40083fd8feeef703d0
Note: switching to '3899edb7f3110d613c72ad40083fd8feeef703d0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 3899edb remove sensitive info
Gurihacker-picoctf@webshell:~/drop-in/drop-in$ git log
Gurihacker-picoctf@webshell:~/drop-in/drop-in$ git checkout 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
Previous HEAD position was 3899edb remove sensitive info
HEAD is now at 6603cb4 create flag
Gurihacker-picoctf@webshell:~/drop-in/drop-in$ grep -r pico
.git/logs/HEAD:0000000000000000000000000000000000000000 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2 picoCTF <ops@picoctf.com> 1710018598 +0000     commit (initial): create flag
.git/logs/HEAD:6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2 3899edb7f3110d613c72ad40083fd8feeef703d0 picoCTF <ops@picoctf.com> 1710018598 +0000     commit: remove sensitive info
.git/logs/HEAD:3899edb7f3110d613c72ad40083fd8feeef703d0 3899edb7f3110d613c72ad40083fd8feeef703d0 Gurihacker-picoctf <Gurihacker-picoctf@webshell.(none)> 1740166586 +0000       checkout: moving from master to 3899edb7f3110d613c72ad40083fd8feeef703d0
.git/logs/HEAD:3899edb7f3110d613c72ad40083fd8feeef703d0 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2 Gurihacker-picoctf <Gurihacker-picoctf@webshell.(none)> 1740166617 +0000       checkout: moving from 3899edb7f3110d613c72ad40083fd8feeef703d0 to 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
.git/logs/refs/heads/master:0000000000000000000000000000000000000000 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2 picoCTF <ops@picoctf.com> 1710018598 +0000        commit (initial): create flag
.git/logs/refs/heads/master:6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2 3899edb7f3110d613c72ad40083fd8feeef703d0 picoCTF <ops@picoctf.com> 1710018598 +0000        commit: remove sensitive info
message.txt:picoCTF{s@n1t1z3_9539be6b}

```
