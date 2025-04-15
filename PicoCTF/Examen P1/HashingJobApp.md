#### Description

If you want to hash with the best, beat this test!

Additional details will be available after launching your challenge instance.
#### Hints 
- You can use a commandline tool or web app to hash text
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.


```
octaviio@LAPTOP-05MLJNS4:~$ echo -n 'a cheap motel' | md5sum
d51908671c7603ec46c7379887509894  -
octaviio@LAPTOP-05MLJNS4:~$ echo -n 'Keanu Reeves' | md5sum
4d2e1f8eabca061706aec58b21c2e199  -
octaviio@LAPTOP-05MLJNS4:~$ echo -n 'Cloude Monet' | md5sum
84e195dd760e6124617f3842bed0d7d8  -
octaviio@LAPTOP-05MLJNS4:~$ echo -n 'Claude Monet' | md5sum
5c37529dab98927d2f3a8da6e8205dcd  -
octaviio@LAPTOP-05MLJNS4:~$

Gurihacker-picoctf@webshell:~$ 
Gurihacker-picoctf@webshell:~$ 
Gurihacker-picoctf@webshell:~$ https://webshell.picoctf.org/
-bash: https://webshell.picoctf.org/: No such file or directory
Gurihacker-picoctf@webshell:~$  echo -n 'a high school bathroom' | md5sum 
98219c442a477b6dc1756d2a6d49d8df  -
Gurihacker-picoctf@webshell:~$ nc saturn.picoctf.net 55706
Please md5 hash the text between quotes, excluding the quotes: 'a cheap motel'
Answer: 
d51908671c7603ec46c7379887509894
d51908671c7603ec46c7379887509894
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Keanu Reeves'
Answer: 
4d2e1f8eabca061706aec58b21c2e199
4d2e1f8eabca061706aec58b21c2e199
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Claude Monet'
Answer: 
84e195dd760e6124617f3842bed0d7d8
84e195dd760e6124617f3842bed0d7d8
Incorrect. Try again?
Answer: 
5c37529dab98927d2f3a8da6e8205dcd
5c37529dab98927d2f3a8da6e8205dcd
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}

```

