Static ain't always noise
### Descripcion

Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh)

### Solucion
```
adrinuquis-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static
--2026-02-10 03:44:55--  https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16776 (16K) [application/octet-stream]
Saving to: 'static'

static                100%[=======================>]  16.38K  --.-KB/s    in 0.006s  

2026-02-10 03:44:55 (2.58 MB/s) - 'static' saved [16776/16776]

adrinuquis-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh
--2026-02-10 03:45:10--  https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh              100%[=======================>]     785  --.-KB/s    in 0s      

2026-02-10 03:45:10 (253 MB/s) - 'ltdis.sh' saved [785/785]

adrinuquis-picoctf@webshell:~$ chmod +x static ltdis.sh
adrinuquis-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
adrinuquis-picoctf@webshell:~$ grep "picoCTF" static.ltdis.strings.txt
   3020 picoCTF{d15a5m_t34s3r_20335e41}
adrinuquis-picoctf@webshell:~$ 
```

picoCTF{d15a5m_t34s3r_20335e41}