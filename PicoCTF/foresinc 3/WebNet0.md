### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

#### hint
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?
# Solución 
primero, descargamos el archivo `capture.pcap` y lo abrimos con Wireshark usando el comando `wireshark capture.pcap &`. Una vez abierto, inspeccionamos pquetes relevantes (como el 6, 13 y 34) usando la opción **Follow → TLS Stream** para analizar las comuniaciones cifradas.

Luego cargamos la llave privada `picopico.key` desde _Edit → Preferences → Protocols → TLS_, lo que permite a Wireshar desencriptar el tráfico. Finalmente, usamos la función de búsqueda (_Edit → Find Next_) para localizar el texto “PicoCTF” y así obtener la banera del reto.
### picoCTF{nongshim.shrimp.crackers}

```


```

