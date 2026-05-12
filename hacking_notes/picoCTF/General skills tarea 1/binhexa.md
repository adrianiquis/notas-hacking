# binhexa
## Descripción

How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance.


## Solución

```
┌──(flavio㉿kali)-[~/Escritorio]
└─$ nc titan.picoctf.net 55459

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11000101
Binary Number 2: 01100111

Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.

Enter the binary result: 01000101
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result:11100111
Correct!

Question 3/6:
Operation 3: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result:110001010
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100101100
Correct!

Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result:110011
Correct!

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100111101000011
Correct!

Enter the results of the last operation in hexadecimal: 4F43

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6ab1ad84}

```

picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6ab1ad84}
## Notas adicionales

Hacemos uso de una pagina convertidora de binarios para las operaciones que nos pide el programa.
## Referencias

[https://www.prepostseo.com/tool/es/binary-to-decimal-converter](https://www.rapidtables.com/calc/math/binary-calculator.html)