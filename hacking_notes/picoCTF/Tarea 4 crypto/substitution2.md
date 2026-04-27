# substitution2

## Descripción

It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher? Download the message [here](https://artifacts.picoctf.net/c/112/message.txt).
## Solución

```
1.-Descargamos y vemos el mensaje
┌──(adrianuquis㉿kali)-[~/picoCTF/Crypto/Tarea-4/substitution2]
└─$ cat message.txt 
nafyffoxenefufytpqnafymfppfentkpxeafbaxraezaqqpzqgswnfyefzwyxnhzqgsfnxnxqlexlzpwbxlrzhkfystnyxqntlbwezhkfyzatppflrfnafefzqgsfnxnxqlevqzwesyxgtyxphqlehenfgetbgxlxenytnxqlvwlbtgflntpemaxzatyfufyhwefvwptlbgtycfntkpfecxppeaqmfufymfkfpxfufnafsyqsfyswysqefqvtaxraezaqqpzqgswnfyefzwyxnhzqgsfnxnxqlxelqnqlphnqnftzautpwtkpfecxppekwntpeqnqrfnenwbflnexlnfyfenfbxltlbfozxnfbtkqwnzqgswnfyezxflzfbfvflexufzqgsfnxnxqletyfqvnflptkqyxqwetvvtxyetlbzqgfbqmlnqywllxlrzafzcpxenetlbfofzwnxlrzqlvxrezyxsneqvvflefqlnafqnafyatlbxeaftuxphvqzwefbqlfospqytnxqltlbxgsyquxetnxqltlbqvnflatefpfgflneqvspthmfkfpxfuftzqgsfnxnxqlnqwzaxlrqlnafqvvflexuffpfgflneqvzqgswnfyefzwyxnhxenafyfvqyftkfnnfyufaxzpfvqynfzafutlrfpxegnqenwbflnexltgfyxztlaxraezaqqpevwynafymfkfpxfufnatntlwlbfyentlbxlrqvqvvflexufnfzalxiwfexefeeflnxtpvqygqwlnxlrtlfvvfznxufbfvfleftlbnatnnafnqqpetlbzqlvxrwytnxqlvqzweflzqwlnfyfbxlbfvflexufzqgsfnxnxqlebqfelqnpftbenwbflnenqclqmnafxyflfghtefvvfznxufphtenftzaxlrnafgnqtznxufphnaxlcpxcftltnntzcfysxzqznvxetlqvvflexufphqyxflnfbaxraezaqqpzqgswnfyefzwyxnhzqgsfnxnxqlnatneffcenqrflfytnfxlnfyfenxlzqgswnfyezxflzftgqlraxraezaqqpfyenftzaxlrnafgflqwratkqwnzqgswnfyefzwyxnhnqsxiwfnafxyzwyxqexnhgqnxutnxlrnafgnqfospqyfqlnafxyqmltlbfltkpxlrnafgnqkfnnfybfvflbnafxygtzaxlfenafvptrxesxzqZNV{L6Y4G_4L41H515_15_73B10W5_8F1KV808} 

2.-Usamos quipqiup
there exist several other well established high school computer security competitions including cyber patriot and us cyber challenge these competitions focus primarily on systems administration fundamentals which are very useful and marketable skills however we believe the proper purpose of a high school computer security competition is not only to teach valuable skills but also to get students interested in and excited about computer science defensive competitions are often laborious affairs and come down to running checklists and executing config scripts offense on the other hand is heavily focused on exploration and improvisation and often has elements of play we believe a competition touching on the offensive elements of computer security is therefore a better vehicle for tech evangelism to students in american high schools further we believe that an understanding of offensive techniques is essential for mounting an effective defense and that the tools and configuration focus encountered in defensive competitions does not lead students to know their enemy as effectively as teaching them to actively think like an attacker pico c t f is an offensively oriented high school computer security competition that seeks to generate interest in computer science among high schoolers teaching them enough about computer security to pique their curiosity motivating them to explore on their own and enabling them to better defend their machines the flag is pico c t f n r m ny due bf

3.-Pasamos a formato picoCTF (la flag final esta mal pero usamos otra pagina para la decodificación, pero con lo que nos dio la pagina anterior dedujimos la flag)
picoCTF{N6R4M_4N41Y515_15_73D10U5_8E1BF808}
```

picoCTF{N6R4M_4N41Y515_15_73D10U5_8E1BF808}
## Notas adicionales


## Referencias