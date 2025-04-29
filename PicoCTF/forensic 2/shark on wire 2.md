## m00nwalk
### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

#### hint
- (None)

# Solución 

```

despues de instalar con el sig comando
python3 -m pip install scapy


hacemos un script
from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''
for p in packets:
	if UDP in p and p[UDP].dport == 22:
		flag += chr(p[UDP].sport - 5000)
print(flag)
y luego lo ejecutamos
python3 exp.py

PicoCTF{P1LLf3r3d_data_v1a_st3g0}
```

