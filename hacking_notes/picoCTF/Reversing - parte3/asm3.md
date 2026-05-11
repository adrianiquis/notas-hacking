## Descripcion

What does asm3(0xdaba8a6c,0xfa8a55d0,0xd7771dae) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/260b193c4ea89ef080c7a828081e482f06628204337fc389755d5de67bd30dcd/test.S)

## Hint

## Solucion


```
┌──(adrianuquis㉿adrianuquis)-[~/Downloads]
└─$ cat test(2).S
asm3:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        <+7>:   xor    eax,eax
        <+9>:   mov    ah,BYTE PTR [ebp+0x9]
        <+12>:  shl    ax,0x10
        <+16>:  sub    al,BYTE PTR [ebp+0xd]
        <+19>:  add    ah,BYTE PTR [ebp+0xf]
        <+22>:  xor    ax,WORD PTR [ebp+0x10]
        <+26>:  nop
        <+27>:  pop    ebp
        <+28>:  ret    


```
#### Stack layout (little-endian, x86 32-bit)

Los argumentos en memoria a partir de `[ebp+0x8]`:

```
Dirección     Bytes (little-endian)
[ebp+0x8]  =  6c 8a ba da   ← arg1: 0xdaba8a6c
[ebp+0xc]  =  d0 55 8a fa   ← arg2: 0xfa8a55d0
[ebp+0x10] =  ae 1d 77 d7   ← arg3: 0xd7771dae
```

Bytes individuales:

```
[ebp+0x9]  = 0x8a
[ebp+0xd]  = 0x55
[ebp+0xf]  = 0xfa  → espera... [ebp+0xc]=d0, [ebp+0xd]=55, [ebp+0xe]=8a, [ebp+0xf]=fa
[ebp+0x10] = 0xae1d (word, little-endian)
```

---

### Ejecución paso a paso

**1.** `xor eax, eax` → `eax = 0x00000000`

**2.** `mov ah, [ebp+0x9]` → `ah = 0x8a`

```
eax = 0x00008a00
```

**3.** `shl ax, 0x10` → shift de 16 bits en AX (16-bit), `ax` se va a 0 (0x8a00 << 16 desborda en 16 bits)

```
ax = 0x0000  →  eax = 0x00000000
```

**4.** `sub al, [ebp+0xd]` → `al = 0x00 - 0x55 = 0xab` (underflow)

```
eax = 0x000000ab
```

**5.** `add ah, [ebp+0xf]` → `ah = 0x00 + 0xfa = 0xfa`

```
eax = 0x0000faab
```

**6.** `xor ax, WORD PTR [ebp+0x10]` → `ax = 0xfaab XOR 0x1dae`

```
  faab = 1111 1010 1010 1011
  1dae = 0001 1101 1010 1110
  XOR  = 1110 0111 0000 0101
       = 0xe705
```

```
eax = 0x0000e705
```

---

### Flag

```
0xe705
```