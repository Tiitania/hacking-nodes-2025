### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
#### hint
- Try using a tool like Wireshark
- How can you decrypt the TLS stream?
# Solución 
Primero, abrimos el archivo `capture.pcap` con Wireshark desde la terminal usando `wireshark capture.pcap &`. Luego, en Wireshark, vamos a _Edit → Preferences → Protocols → TLS_ para cargar la llave privada `picopico.key`, lo que permite desencriptar el tráfico (indicados en verde).

Después, buscamos el paquete 47, vamos a _File → Export Objects → HTTP_ y exportamos el objeto del paquete 91, que es una imagen (`vulture.jpg`). Finalmente, en la terminal, usamos `strings vulture.jpg` para analizar el contenido oculto de la imagen, donde encontramos la bandera del reto.
### picoCTF{honey.roasted.peanuts}