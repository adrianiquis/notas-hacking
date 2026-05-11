### Descripcion

What does asm1(0xe26) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/c7ce5cfbb522cd448de7adcb1dc42106af4f859002381aa47d85b45cc66aa3f2/test.S)

## Hint

assembly conditions

## Solución

```
┌──(adrianuquis㉿adrianuquis)-[~/Downloads]
└─$ cat test.S          
asm1:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        <+7>:   cmp    DWORD PTR [ebp+0x8],0x75b
        <+14>:  jg     0x11d6 <asm1+41>
        <+16>:  cmp    DWORD PTR [ebp+0x8],0x34b
        <+23>:  jne    0x11ce <asm1+33>
        <+25>:  mov    eax,DWORD PTR [ebp+0x8]
        <+28>:  add    eax,0x13
        <+31>:  jmp    0x11ed <asm1+64>
        <+33>:  mov    eax,DWORD PTR [ebp+0x8]
        <+36>:  sub    eax,0x13
        <+39>:  jmp    0x11ed <asm1+64>
        <+41>:  cmp    DWORD PTR [ebp+0x8],0xe26
        <+48>:  jne    0x11e7 <asm1+58>
        <+50>:  mov    eax,DWORD PTR [ebp+0x8]
        <+53>:  sub    eax,0x13
        <+56>:  jmp    0x11ed <asm1+64>
        <+58>:  mov    eax,DWORD PTR [ebp+0x8]
        <+61>:  add    eax,0x13
        <+64>:  pop    ebp
        <+65>:  ret    


```

**Paso 1:** `cmp 0xe26, 0x75b` → ¿Es 0xe26 > 0x75b?

- 0xe26 = 3622, 0x75b = 1883 → **SÍ** → salta a `+41`

**Paso 2:** En `+41`: `cmp 0xe26, 0xe26` → ¿Son iguales?

- **SÍ** → **NO** salta (jne no se cumple) → continúa en `+50`

**Paso 3:** En `+50`:

asm

```asm
mov eax, [ebp+0x8]   ; eax = 0xe26
sub eax, 0x13         ; eax = 0xe26 - 0x13 = 0xe13
jmp +64               ; retorna
```

---

### Resultado

```
0xe26 - 0x13 = 0xe13
```

### Flag

```
0xe13
```

