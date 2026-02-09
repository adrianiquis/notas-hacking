### Descripcion
There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 60944, but it doesn't speak English...

### Solucion

```
adrinuquis-picoctf@webshell:~$ nc wily-courier.picoctf.net 60944
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
97 
57 
52 
101 
55 
125 
10 
adrinuquis-picoctf@webshell:~$ python3 -c 'print("".join([chr(n) for n in [112, 105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 97, 57, 52, 101, 55, 125]]))'
picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}
```

picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}