### Description
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)


#### hint
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}
# Solución 
en este reto tiene la idea de ser como las muñecas rusas  matryoshka el binkwalk lo usaremos para analizar y extraer automaticamente ls archivos ocultos dentro del archivo

```
Gurihacker-picoctf@webshell:~$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383940, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22

Gurihacker-picoctf@webshell:~$ cd _dolls.jpg.extracted/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted$ ls
4286C.zip  base_images
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted$ cd base_images/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ ls
2_c.jpg
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196045, uncompressed size: 201447, name: base_images/3_c.jpg
383807        0x5DB3F         End of Zip archive, footer length: 22
383918        0x5DBAE         End of Zip archive, footer length: 22

Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ cd base_images/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ 3_c.jpg
-bash: 3_c.jpg: command not found
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$  binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77653, uncompressed size: 79808, name: base_images/4_c.jpg
201425        0x312D1         End of Zip archive, footer length: 22

Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ ls
1E2D6.zip  base_images
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ cd base_images/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 64, uncompressed size: 81, name: flag.txt
79786         0x137AA         End of Zip archive, footer length: 22

Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ vi flag.txt 

[1]+  Stopped                 vi flag.txt
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt 
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ^C
Gurihacker-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ 

```

