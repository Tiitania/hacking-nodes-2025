## m00nwalk
### Description

Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.

#### hint
- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option


# Solución 

```

recibios un .wav, el sonido puede sacar una imagen, esto ya se hacía desde hace mucho
en este caso para poder realizarlo es con el SSTV DECODER 
usamos el comando: sstv -d message.wav -o flag.png
abrimos la imagen y nos muestra una imagen y en un lugar sale el comando:

picoCTF{beep_boop_im_in_space}

```

