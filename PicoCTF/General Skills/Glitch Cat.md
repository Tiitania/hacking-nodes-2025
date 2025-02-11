## Glitch Cat
### Description

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance

La instancia en cuestión:
```
nc saturn.picoctf.net 50028
```
#### hint
- ASCII is one of the most common encodings used in programming
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

# Solución 
la solución lo hice mediante python, mostraba la bandera pero con caracteres ascci, por lo que lo junté todo en un print 
```
print('gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35))

PS D:\python> & C:/Users/pando/AppData/Local/Programs/Python/Python313/python.exe "d:/python/keku ascci.py"
gl17ch_m3_n07_bda68f75

picoCTF{gl17ch_m3_n07_bda68f75}
```

