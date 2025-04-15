#### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py) using [this password](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt) to get [the flag](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en)?

#### Hints 
- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py
	- $ man python


```
Gurihacker-picoctf@webshell:~$ cat pw.txt 
aa821c16aa821c16aa821c16aa821c16
Gurihacker-picoctf@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:aa821c16aa821c16aa821c16aa821c16
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}
```

