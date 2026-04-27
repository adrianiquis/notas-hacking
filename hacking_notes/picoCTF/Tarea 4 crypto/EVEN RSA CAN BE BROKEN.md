# EVEN RSA CAN BE BROKEN???

## Descripción

This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 62626` The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/2b0f68c54cfcb2dafd4ca90c4abcbe73c208f09edf65af336fc7023e1c1314ca/encrypt.py).
## Solución

```
1.-Descargamos el archivo python y vemos el mensaje 

┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/evenRSABEBRK]
└─$ nc verbal-sleep.picoctf.net 62626
N: 17870523984271322725603520073228059543460231528238010156623516754588717115824796488686162783679607026058577501262758832500258785738012389714687317567958198
e: 65537
cyphertext: 5669493782753348580954687189943927934966817740931047741509642034177886055785875983030959059495706605048678535540729109814994412176223017287418046878932917

2.-Usamos otro código por tema de dependencias
# Valores

n = 17870523984271322725603520073228059543460231528238010156623516754588717115824796488686162783679607026058577501262758832500258785738012389714687317567958198

e = 65537

c = 5669493782753348580954687189943927934966817740931047741509642034177886055785875983030959059495706605048678535540729109814994412176223017287418046878932917

  

# 1. Factorización trivial (porque N es par)

p = 2

q = n // 2

  

# 2. Calculamos la función indicatriz de Euler (phi)

phi = (p - 1) * (q - 1)

  

# 3. Calculamos la clave privada 'd' (inverso modular de e mod phi)

# Python >3.8 permite pasar -1 como exponente en pow() para sacar el inverso

d = pow(e, -1, phi)

  

# 4. Desciframos el texto cifrado

m = pow(c, d, n)

  

# 5. Convertimos el número resultante a texto

flag_bytes = m.to_bytes((m.bit_length() + 7) // 8, byteorder='big')

print("Flag:", flag_bytes.decode('utf-8'))

3.-Ejecutamos el script
┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/evenRSABEBRK]
└─$ python3 solucion.py     
Flag: picoCTF{tw0_1$_pr!m31c9046c4}
```

picoCTF{tw0_1$_pr!m31c9046c4}
## Notas adicionales


## Referencias