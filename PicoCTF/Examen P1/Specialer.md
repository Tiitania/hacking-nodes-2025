#### Description

Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.

Additional details will be available after launching your challenge instance.

#### Hints 
- What programs do you have access to?
- 


```

octaviio@LAPTOP-05MLJNS4:~$ ssh -p 57870 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:57870 ([13.59.203.175]:57870)' can't be established.
ECDSA key fingerprint is SHA256:dJtvF/J5LfkJcePCA5aEPg1zZbM6yb37NnsNhGVyygI.
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[saturn.picoctf.net]:57870,[13.59.203.175]:57870' (ECDSA) to the list of known hosts.
Specialer$ echo "$(<abra/cadabra.txt)"
Nothing up my sleeve!
Specialer$ echo */*
abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ echo "$(<abra/cadaniel.txt)"
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ echo "$(<ala/kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}


```

