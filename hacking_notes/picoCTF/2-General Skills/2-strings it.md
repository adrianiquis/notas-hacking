Strings it

### Descripcion
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/6577d3f1500aebcd300787bd5d96216b30aed379c811f5e83e888f897da4a3d5/strings) without running it?

### Solucion
```
adrinuquis-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/6577d3f1500aebcd300787bd5d96216b30aed379c811f5e83e888f897da4a3d5/strings
--2026-02-10 03:37:19--  https://challenge-files.picoctf.net/c_fickle_tempest/6577d3f1500aebcd300787bd5d96216b30aed379c811f5e83e888f897da4a3d5/strings
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.64, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 784424 (766K) [application/octet-stream]
Saving to: 'strings'

strings               100%[=======================>] 766.04K  1.83MB/s    in 0.4s    

2026-02-10 03:37:19 (1.83 MB/s) - 'strings' saved [784424/784424]

adrinuquis-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_d6306c19}
```

picoCTF{5tRIng5_1T_d6306c19}


