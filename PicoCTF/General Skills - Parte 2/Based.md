### Description
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.
#### hint
- I hear python can convert things.
- It might help to have multiple windows open.

# Solución 

````
Gurihacker-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.
...
you have 45 seconds.....

Input:
chair
Please give me the  154 151 147 150 164 as a word.
Input:
light
Please give me the 706965 as a word.
Input:
pie
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
^C
Gurihacker-picoctf@webshell:~$ 
```
``


````

Usando el CyberChef la solución quedaría como
from binary
````
Input: 01100011 01101000 01100001 01101001 01110010

Recipe:From Binary

Output: chair

Input: 154 151 147 150 164

Recipe:From octal

Output: light

Input: 706965

Recipe:From hex

Output: pie



```
