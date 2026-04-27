# rail-fence

## Descripción

A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://artifacts.picoctf.net/c/189/message.txt). Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
## Solución

```
1.-Descargamos y vemos le mensaje
┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/railfence]
└─$ cat message.txt  
Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6

2.-Usamos cyberchef para decifrarlo (link en referencias)
The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7

3.-Pasamos al formato de picoCTF
picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}
```

picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}
## Notas adicionales


## Referencias

https://en.wikipedia.org/wiki/Rail_fence_cipher

https://gchq.github.io/CyberChef/#recipe=Rail_Fence_Cipher_Decode(4,0)&input=VGEgXzdONkQ4RGhsZzpXM0RfSDNDMzFOX18zODdlZiBzSFIwNTNGMzhONDNERkQgaTMzX19fTjY