## Collaborative Development
### Description 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)

### Hint

- `git branch -a` will let you see available branches
- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

## Solución 
```
picoCTF{t3@mw0rk_Gurihacker-picoctf@webshell:~/drop-in$ git checkout  feature/part-2
Switched to branch 'feature/part-2'
Gurihacker-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
m@k3s_th3_dr3@m_Gurihacker-picoctf@webshell:~/drop-in$ git checkout  feature/part-1
Switched to branch 'feature/part-1'
Gurihacker-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
picoCTF{t3@mw0rk_Gurihacker-picoctf@webshell:~/drop-in$ ^C
Gurihacker-picoctf@webshell:~/drop-in$ git checkout  feature/part-3
Switched to branch 'feature/part-3'
Gurihacker-picoctf@webshell:~/drop-in$ python flag.py
Printing the flag...
w0rk_2c91ca76}

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}

```
