# Collaborative Development
## Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)
## Solución

```
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ wget https://artifacts.picoctf.net/c_titan/69/challenge.zip

┌──(adri㉿kali)-[~/Escritorio]
└─$ ls
challenge.zip  drop-in
                                                                             
┌──(adri㉿kali)-[~/Escritorio]
└─$ cd drop-in/
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ ls
flag.py
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ python3 flag.py   
Printing the flag...
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git log flag.py   
commit eb4de2a9826332633c62e44a1a130d9b1a88171a (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    init flag printer
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git log        
commit eb4de2a9826332633c62e44a1a130d9b1a88171a (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    init flag printer
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
  
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git checkout feature/part-1      
Cambiado a rama 'feature/part-1'
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git show                   
commit ad37f59bfdcb1e8052bf7e12e1d89a2adb315cf9 (HEAD -> feature/part-1)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 1

diff --git a/flag.py b/flag.py
index 77d6cec..6e17fb3 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,2 @@
 print("Printing the flag...")
+print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git checkout feature/part-2
Cambiado a rama 'feature/part-2'
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git show                   
commit 9792a89fa347abc711f84b7208db18d164d45aca (HEAD -> feature/part-2)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 2

diff --git a/flag.py b/flag.py
index 77d6cec..7ab4e25 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("m@k3s_th3_dr3@m_", end='')
\ No newline at end of file
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git checkout feature/part-3
Cambiado a rama 'feature/part-3'
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git show                   
commit 1308521d0d0b66df1a73e91d5d9e2d74610002e3 (HEAD -> feature/part-3)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:38 2024 +0000

    add part 3

diff --git a/flag.py b/flag.py
index 77d6cec..78ac69c 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("w0rk_e4b79efb}")
```

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
## Notas adicionales

Para este reto hacemos uso de git checkout para cambiar entre ramas y asi revisar los commits donde esta la flag
## Referencias