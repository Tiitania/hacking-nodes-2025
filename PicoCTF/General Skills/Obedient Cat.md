## Obedient Cat

This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).

#### hint
- Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag`
- $ man cat

# Solución 1
la solución es con el cmd de linux en este caso webshell usando cat -A para abrir nuestro archivo
```
Gurihacker-picoctf@webshell:~$ cat flag  -A
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}$

```
