

## Descripción

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/bfbfec697635785f9c857dc66f592c111a0af651ba20e5e18d9a15096dd19dd5/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/bfbfec697635785f9c857dc66f592c111a0af651ba20e5e18d9a15096dd19dd5/scrambled2.png)
## Solución

```
#Usamos el siguiente código para unir las 2 imagenes

from PIL import Image # pip install Pillow

img1 = Image.open("scrambled1.png")

pixels1 = img1.load()

img2 = Image.open("scrambled2.png")

  

pixels2 = img2.load()

  

flag = Image.new("RGB" ,img1.size)

flagpix = flag.load()

for row in range(img1.size[1]):

for col in range(img1.size[0]):

flagpix[col,row]=(

(pixels1[col,row][0]+pixels2[col,row][0])%256,

(pixels1[col,row][1]+pixels2[col,row][1])%256,

(pixels1[col,row][2]+pixels2[col,row][2])%256)

flag.save("flag.png")

#Nos regresa una imagen con la flag

picoCTF{8cdf93c3}
```

picoCTF{8cdf93c3}
## Notas adicionales


## Referencias

https://en.wikipedia.org/wiki/Visual_cryptography