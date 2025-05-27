#### Description

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)
#### Hints 
-Bits are expensive, I used only a little bit over 100 to save money

```
Gurihacker-picoctf@webshell:~$ cat values 
Decrypt my super sick RSA:
c: 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n: 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e: 65537Gurihacker-picoctf@webshell:~$ ^C

}

>>> c = 861270243527190895777142537838333832920579264010533029282104230006461420086153423
>>>
>>> n = 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
>>>
>>> e = 65537
>>> p = 1955175890537890492055221842734816092141
>>> q = 670577792467509699665091201633524389157003
>>> tn = (p-1) * (q-1)
>>> d = pow(e, -1, tn)
>>> m = pow(c, d, n)
>>> plaintext = bytes.fromhex(hex(m)[2:])
>>> plaintext = bytes.fromhex(hex(m)[2:])
>>>
>>> print(plaintext.decode())
picoCTF{sma11_N_n0_g0od_13686679}


```

## Referencias
https://factordb.com/index.php?query=1311097532562595991877980619849724606784164430105441327897358800116889057763413423