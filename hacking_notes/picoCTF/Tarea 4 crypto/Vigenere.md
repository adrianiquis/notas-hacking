# Vigenere

## Descripción

Can you decrypt this message? Decrypt this [message](https://artifacts.picoctf.net/c/160/cipher.txt) using this key "CYLAB".
## Solución

```
1.-Descargamos y vemos el mensaje

┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/vigenere]
└─$ cat cipher.txt 
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}

2.-Usamos cypherchef para decifrar con Vigenere (Key CYLAB)
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}
```

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}
## Notas adicionales


## Referencias

https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher


https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('CYLAB')&input=cmdub0RWRHtPME5VX1dRM19HMUczTzNUM19BMUFIM1NfMjk1MWM4OWZ9Cg&oenc=65001