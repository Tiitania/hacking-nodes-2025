### Includes
### Description 

Can you get the flag?Go to this [website](http://saturn.picoctf.net:61253/) and see what you can discover.
### Hint

- Is there more code than what the inspector initially shows?

## Solución  1
```
http://saturn.picoctf.net:61253/style.css
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */

http://saturn.picoctf.net:61253/script.js
  
function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_b8f4b022}

picoCTF{1nclu51v17y_1of2_f7w_2of2_b8f4b022}
```