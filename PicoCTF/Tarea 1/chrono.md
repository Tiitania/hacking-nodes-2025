## chrono
### Description 
How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance.
### Hint
- (None)

## Solución 
```
icoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

nos interesa el challenge , no nos deja entrar por lo que usamos un grep 
picoplayer@challenge:/$ grep -r pico
grep: etc/.pwd.lock: Permission denied
etc/group:picoplayer:x:1000:
grep: etc/gshadow: Permission denied
etc/passwd:picoplayer:x:1000:1000::/home/picoplayer:/bin/bash
grep: etc/security/opasswd: Permission denied
grep: etc/shadow: Permission denied
etc/subgid:picoplayer:100000:65536
etc/subuid:picoplayer:100000:65536
grep: etc/ssh/ssh_host_ecdsa_key: Permission denied
grep: etc/ssh/ssh_host_ed25519_key: Permission denied
grep: etc/ssh/ssh_host_rsa_key: Permission denied
grep: etc/ssh/ssh_host_dsa_key: Permission denied
etc/crontab:# picoCTF{Sch3DUL7NG_T45K3_L1NUX_9d5cb744}

```
