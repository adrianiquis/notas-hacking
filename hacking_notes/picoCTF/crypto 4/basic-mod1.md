# basic-mod1

## Descripción

We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/127/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución

```
#Usamos el siguiente código de python
# Lista de números del mensaje interceptado
mensaje = [128, 322, 353, 235, 336, 73, 198, 332, 202, 285, 57, 87, 262, 221, 218, 405, 335, 101, 256, 227, 112, 140]

# Construimos el conjunto de caracteres según las reglas
# 0-25: A-Z
# 26-35: 0-9
# 36: _
caracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"

# Variable para guardar el texto descifrado
texto_descifrado = ""

# Iteramos sobre cada número del mensaje
for numero in mensaje:
    # Obtenemos el módulo 37
    indice = numero % 37
    # Añadimos el carácter correspondiente usando el índice
    texto_descifrado += caracteres[indice]

# Imprimimos el resultado con el formato de la bandera
bandera = f"picoCTF{{{texto_descifrado}}}"
print("¡Bandera descifrada!")
print(bandera)

¡Bandera descifrada!
picoCTF{R0UND_N_R0UND_79C18FB3}
```

picoCTF{R0UND_N_R0UND_79C18FB3}
## Notas adicionales


## Referencias