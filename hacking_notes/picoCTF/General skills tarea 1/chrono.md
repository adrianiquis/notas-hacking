# chrono
## Descripción

How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance.

Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 55133
Username: picoplayer 
Password: kZx-HVJKu8
```
## Solución

```
┌──(adri㉿kali)-[~/Escritorio]
└─$ ssh -p 55133 picoplayer@saturn.picoctf.net

picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```

picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
## Notas adicionales

En este reto no nos dan instrucciones claras, lo que si nos dan es una pista de en que carpeta puede estar la flag y ya solo es buscar con el comando "cat".
## Referencias

https://www.redeszone.net/tutoriales/servidores/cron-crontab-linux-programar-tareas/