
## Descripcion

What does asm2(0x8,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/e52eb78a50fe37d5d90fa3200de17edb7b6e51a3e01c583cec0ed94d9e9bc306/test.S)

## Hints

## Solucion

```
┌──(adrianuquis㉿adrianuquis)-[~/Downloads]
└─$ cat test(1).S
asm2:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        <+7>:   sub    esp,0x10
        <+10>:  mov    eax,DWORD PTR [ebp+0xc]
        <+13>:  mov    DWORD PTR [ebp-0x4],eax
        <+16>:  mov    eax,DWORD PTR [ebp+0x8]
        <+19>:  mov    DWORD PTR [ebp-0x8],eax
        <+22>:  jmp    0x11d0 <asm2+35>
        <+24>:  add    DWORD PTR [ebp-0x4],0x1
        <+28>:  add    DWORD PTR [ebp-0x8],0xed
        <+35>:  cmp    DWORD PTR [ebp-0x8],0xe6da
        <+42>:  jle    0x11c5 <asm2+24>
        <+44>:  mov    eax,DWORD PTR [ebp-0x4]
        <+47>:  leave  
        <+48>:  ret    

 
```

**Argumentos:**

- `[ebp+0x8] = 0x8` (primer argumento)
- `[ebp+0xc] = 0x2e` (segundo argumento)

**Variables locales inicializadas:**

```
[ebp-0x4] = 0x2e   (copia del 2do arg)
[ebp-0x8] = 0x8    (copia del 1er arg)
```

---

### Es un bucle

```
jmp → condición
  si [ebp-0x8] <= 0xe6da → vuelve al inicio
  si no → retorna [ebp-0x4]
```

Cada iteración:

- `[ebp-0x4] += 0x1`
- `[ebp-0x8] += 0xed`

---

### Calculando cuántas iteraciones

Necesitamos que `[ebp-0x8] > 0xe6da`:

```
0x8 + (n × 0xed) > 0xe6da
n > (0xe6da - 0x8) / 0xed
n > 0xe6d2 / 0xed
n > 59090 / 237
n > 249.32...
→ n = 250 iteraciones
```

### Valor de retorno

```
[ebp-0x4] = 0x2e + 250
           = 46  + 250
           = 296
           = 0x128
```

---

### Flag

```
0x128
```
