# Picker IV

## Descripción

Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 62769` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV).
## Solución

```
1.-Descargamos los archivos y los visualizamos

#include <stdio.h>

#include <stdlib.h>

#include <signal.h>

#include <unistd.h>

  
  

void print_segf_message(){

printf("Segfault triggered! Exiting.\n");

sleep(15);

exit(SIGSEGV);

}

  

int win() {

FILE *fptr;

char c;

  

printf("You won!\n");

// Open file

fptr = fopen("flag.txt", "r");

if (fptr == NULL)

{

printf("Cannot open file.\n");

exit(0);

}

  

// Read contents from file

c = fgetc(fptr);

while (c != EOF)

{

printf ("%c", c);

c = fgetc(fptr);

}

  

printf("\n");

fclose(fptr);

}

  

int main() {

signal(SIGSEGV, print_segf_message);

setvbuf(stdout, NULL, _IONBF, 0); // _IONBF = Unbuffered

  

unsigned int val;

printf("Enter the address in hex to jump to, excluding '0x': ");

scanf("%x", &val);

printf("You input 0x%x\n", val);

  

void (*foo)(void) = (void (*)())val;

foo();

}

2.-Gracias a que nos dan el binario, podemos usar el comando objdump el cual nos da info extra del propio binario que combinandolo con grep nos da el hexadecimal al cual queremos ir (la función win)

┌──(adri㉿kali)-[~/picoCTF/Reversing/Picker4]
└─$ objdump -D picker-IV | grep win
000000000040129e <win>:
  4012d2:       75 16                   jne    4012ea <win+0x4c>
  4012f9:       eb 1a                   jmp    401315 <win+0x77>
  401319:       75 e0                   jne    4012fb <win+0x5d>
                                                                                                                                                                                                                                           
┌──(adri㉿kali)-[~/picoCTF/Reversing/Picker4]
└─$ nc saturn.picoctf.net 62769
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
```

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
## Notas adicionales


## Referencias