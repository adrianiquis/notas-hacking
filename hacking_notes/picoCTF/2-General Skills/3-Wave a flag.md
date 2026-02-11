Wave a flag

###  Descricpion
Can you invoke help flags for a tool or binary? This program haz extraordinarly helpful information

### Solucion
```
adrinuquis-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
--2026-02-10 03:41:12--  https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                  100%[=======================>]  18.86K  --.-KB/s    in 0.006s  

2026-02-10 03:41:12 (3.25 MB/s) - 'warm' saved [19312/19312]

adrinuquis-picoctf@webshell:~$ chmod +x warm
adrinuquis-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```

