## fixme1.py
### Description 
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

### Hint
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.


## Solución 1
la solución es en la parte del printf, esta en mal sintaxis y la identidad del flag era otra

```
Gurihacker-picoctf@webshell:~$ python fixme1.py
Traceback (most recent call last):
  File "/home/Gurihacker-picoctf/fixme1.py", line 21, in <module>
    print("That is correct! Here\'s your flag: " + flag)
NameError: name 'flag' is not defined. Did you mean: 'lag'?
Gurihacker-picoctf@webshell:~$ nano fixme1.py
Gurihacker-picoctf@webshell:~$ python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```



