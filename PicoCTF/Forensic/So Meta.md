
#### Description

Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).

## Hint
What does meta mean in the context of files?
Ever heard of metadata?

## Solución
```
octaviio@LAPTOP-05MLJNS4:~/SO$ exiftool pico_img.png -Artist -Filter
Artist                          : picoCTF{s0_m3ta_d8944929}
Filter                          : Adaptive
octaviio@LAPTOP-05MLJNS4:~/SO$
```