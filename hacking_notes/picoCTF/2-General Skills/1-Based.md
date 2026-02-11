Based
### Descripción

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?Connect with nc fickle-tempest.picoctf.net 61119.
### Solución
```
adrinuquis-picoctf@webshell:~$ nc wily-courier.picoctf.net 60944
adrinuquis-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 53925             
Let us see how data is stored
colorado
Please give the 01100011 01101111 01101100 01101111 01110010 01100001 01100100 01101111 as a word.
...
you have 45 seconds.....

Input:
colorado
Please give me the  o154 o151 o155 o145 as a word.
Input:
limeToo slow!

adrinuquis-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 53925
Let us see how data is stored
computer
Please give the 01100011 01101111 01101101 01110000 01110101 01110100 01100101 01110010 as a word.
...
you have 45 seconds.....

Input:
computer
Please give me the  o154 o151 o172 o141 o162 o144 as a word.
Input:
lizard
Please give me the 66616c636f6e as a word.
Input:
falcon
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_6c3Fb625}
```

picoCTF{learning_about_converting_values_6c3Fb625}

### Notas
Utilice el traductor de cyberchef para traducir de binario, octal y hexagonal
### Referencias
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDExMDAwMTEgMDExMDExMTEgMDExMDExMDEgMDExMTAwMDAgMDExMTAxMDEgMDExMTAxMDAgMDExMDAxMDEgMDExMTAwMTA&ieol=CRLF&oeol=VT

[https://gchq.github.io/CyberChef/#recipe=Decode_text('UTF-8%20(65001)')From_Binary('Space',8)&input=DQowMTExMDAxMSAwMTEwMTEwMCAwMTExMDEwMSAwMTEwMDEwMCAwMTEwMDExMSAwMTEwMDEwMQ&ieol=CRLF](https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTU0IDE1MSAxNzIgMTQxIDE2MiAxNDQ)
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NjY2MTZjNjM2ZjZl&oeol=FF

