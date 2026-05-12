# time machine
## Descripción

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)
## Solución

```
┌──(adri㉿kali)-[~/Escritorio]
└─$ wget https://artifacts.picoctf.net/c_titan/162/challenge.zip

┌──(adri㉿kali)-[~/Escritorio]
└─$ ls
challenge.zip  drop-in
                                                                             
┌──(adri㉿kali)-[~/Escritorio]
└─$ cd drop-in/
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ ls
message.txt
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git show
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}

diff --git a/message.txt b/message.txt
new file mode 100644
index 0000000..4324621
--- /dev/null
+++ b/message.txt
@@ -0,0 +1 @@
+This is what I was working on, but I'd need to look at my commit history to know why...
\ No newline at end of file
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git reflog                                                  
712314f (HEAD -> master) HEAD@{0}: commit (initial): picoCTF{t1m3m@ch1n3_e8c98b3a}
                                                                             
┌──(adri㉿kali)-[~/Escritorio/drop-in]
└─$ git log                                                     
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
```

picoCTF{t1m3m@ch1n3_e8c98b3a}
## Notas adicionales

podemos usar "git reflog" o "git log" para ver los commits y comentarios al hacerles pull.
## Referencias