## Descripcion

Using a Secure Shell (SSH) is going to be pretty important.Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `54916` to get the flag?You'll also need the password `84b12bae`. If asked, accept the fingerprint with `yes`.If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
### Hints

# Solucion

1. Corremos la instancia privada
2. Nos conectamos por medio de ssh
    1. `ssh ctf-player@titan.picoctf.net -p 55308`
    2. Escribimos la contraseña que nos da el propio reto.
3. Ingresar la flag:

```
picoCTF{s3cur3_c0nn3ct10n_07a987ac}
```

### Referencias