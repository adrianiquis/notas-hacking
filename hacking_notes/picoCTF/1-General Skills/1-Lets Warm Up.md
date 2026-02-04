1-Lets Warm up

Descripcion
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

Solucion
 - Usando cyberchef
 - https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA

Solucion 2
- Usando pyhton
```
- adrinuquis-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.>>> 
>>> int(0x70)
112
>>> chr(112)
'p'
>>> ord('p')
112
>>> 
```

picoCTF{p}

notas
- utilizamoscyberchef para 
referencia
