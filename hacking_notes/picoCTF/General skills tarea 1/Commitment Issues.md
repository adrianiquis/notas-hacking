# Commitment Issues
## Descripción


## Solución

```
┌──(adri㉿kali)-[~/Escritorio]
└─$ wget https://artifacts.picoctf.net/c_titan/139/challenge.zip

┌──(adri㉿kali)-[~/Escritorio]
└─$ ls
challenge.zip
                                                                             
┌──(adri㉿kali)-[~/Escritorio]
└─$ unzip challenge.zip

┌──(adri㉿kali)-[~/Escritorio]
└─$ cd drop-in 

┌──(adri㉿kali)-[~/Escritorio]
└─$ ls
message.txt

┌──(adri㉿kali)-[~/Escritorio]
└─$ cat message.txt
TOP SECRET

┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git show            
commit 144fdc44b09058d7ea7f224121dfa5babadddbb9 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    remove sensitive info

diff --git a/message.txt b/message.txt
index 3a71673..d552d1e 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-picoCTF{s@n1t1z3_be3dd3da}
+TOP SECRET
```

picoCTF{s@n1t1z3_be3dd3da}
## Notas adicionales

Con "git show" muestra el ultimo commit con diferencia al anterior lo que no permite encontrar la flag antes de que cambiara con el commit
## Referencias

https://primer.picoctf.org/#_git_version_control