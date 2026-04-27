# substitution0

## Descripción

A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? Download the message [here](https://artifacts.picoctf.net/c/153/message.txt).
## Solución

```
1.-Descargamos y vemos el mensaje
┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/substitution0]
└─$ cat message.txt 
OHNFUMWSVZLXEGCPTAJDYIRKQB 

Suauypcg Xuwaogf oacju, rvds o waoiu ogf jdoduxq ova, ogf hacywsd eu dsu huudxu
mace o wxojj noju vg rsvns vd roj ugnxcjuf. Vd roj o huoydvmyx jnoaohouyj, ogf, od
dsod dveu, yglgcrg dc godyaoxvjdj—cm ncyaju o wauod pavbu vg o jnvugdvmvn pcvgd
cm ivur. Dsuau ruau drc acygf hxonl jpcdj guoa cgu ukdauevdq cm dsu honl, ogf o
xcgw cgu guoa dsu cdsua. Dsu jnoxuj ruau uknuufvgwxq soaf ogf wxcjjq, rvds oxx dsu
oppuoaognu cm hyagvjsuf wcxf. Dsu ruvwsd cm dsu vgjund roj iuaq aueoalohxu, ogf,
dolvgw oxx dsvgwj vgdc ncgjvfuaodvcg, V ncyxf soafxq hxoeu Zypvdua mca svj cpvgvcg
aujpundvgw vd.

Dsu mxow vj: pvncNDM{5YH5717Y710G_3I0XY710G_03055505} 

2.-Usamos cyberchef con Substitution
Plaintext:OHNFUMWSVZLXEGCPTAJDYIRKQBohnfumwsvzlxegcptajdyirkqb
CipherText:ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz

ABCDEFGHIJKLMNOPQRSTUVWXYZ 

Hereupon Legrand arose, with a grave and stately air, and brought me the beetle
from a glass case in which it was enclosed. It was a beautiful scarabaeus, and, at
that time, unknown to naturalists—of course a great prize in a scientific point
of view. There were two round black spots near one extremity of the back, and a
long one near the other. The scales were exceedingly hard and glossy, with all the
appearance of burnished gold. The weight of the insect was very remarkable, and,
taking all things into consideration, I could hardly blame Jupiter for his opinion
respecting it.

The flag is: picoCTF{5UB5717U710N_3V0LU710N_03055505}
```

picoCTF{5UB5717U710N_3V0LU710N_03055505}
## Notas adicionales


## Referencias
https://gchq.github.io/CyberChef/#recipe=Substitute('OHNFUMWSVZLXEGCPTAJDYIRKQBohnfumwsvzlxegcptajdyirkqb','ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz',false)&input=T0hORlVNV1NWWkxYRUdDUFRBSkRZSVJLUUIgCgpTdWF1eXBjZyBYdXdhb2dmIG9hY2p1LCBydmRzIG8gd2FvaXUgb2dmIGpkb2R1eHEgb3ZhLCBvZ2YgaGFjeXdzZCBldSBkc3UgaHV1ZHh1Cm1hY2UgbyB3eG9qaiBub2p1IHZnIHJzdm5zIHZkIHJvaiB1Z254Y2p1Zi4gVmQgcm9qIG8gaHVveWR2bXl4IGpub2FvaG91eWosIG9nZiwgb2QKZHNvZCBkdmV1LCB5Z2xnY3JnIGRjIGdvZHlhb3h2amRq4oCUY20gbmN5YWp1IG8gd2F1b2QgcGF2YnUgdmcgbyBqbnZ1Z2R2bXZuIHBjdmdkCmNtIGl2dXIuIERzdWF1IHJ1YXUgZHJjIGFjeWdmIGh4b25sIGpwY2RqIGd1b2EgY2d1IHVrZGF1ZXZkcSBjbSBkc3UgaG9ubCwgb2dmIG8KeGNndyBjZ3UgZ3VvYSBkc3UgY2RzdWEuIERzdSBqbm94dWogcnVhdSB1a251dWZ2Z3d4cSBzb2FmIG9nZiB3eGNqanEsIHJ2ZHMgb3h4IGRzdQpvcHB1b2FvZ251IGNtIGh5YWd2anN1ZiB3Y3hmLiBEc3UgcnV2d3NkIGNtIGRzdSB2Z2p1bmQgcm9qIGl1YXEgYXVlb2Fsb2h4dSwgb2dmLApkb2x2Z3cgb3h4IGRzdmd3aiB2Z2RjIG5jZ2p2ZnVhb2R2Y2csIFYgbmN5eGYgc29hZnhxIGh4b2V1IFp5cHZkdWEgbWNhIHN2aiBjcHZndmNnCmF1anB1bmR2Z3cgdmQuCgpEc3UgbXhvdyB2ajogcHZuY05ETXs1WUg1NzE3WTcxMEdfM0kwWFk3MTBHXzAzMDU1NTA1fQ&oenc=65001