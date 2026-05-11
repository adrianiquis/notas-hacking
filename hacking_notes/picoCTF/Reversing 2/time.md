# time

## Descripción

You will find the flag after analysing this apk Download [here](https://artifacts.picoctf.net/c/449/timer.apk).
## Solución

```
1.-Descargamos el archivo
2.-Instalamos un comando externo "apktool"
3.-Analizamos el apk 

┌──(flavio㉿kali)-[~/picoCTF/Reversing/timer]
└─$ apktool d timer.apk  
I: Using Apktool 2.7.0-dirty on timer.apk
I: Loading resource table...
I: Decoding AndroidManifest.xml with resources...
I: Loading resource table from file: /home/flavio/.local/share/apktool/framework/1.apk
I: Regular manifest package...
I: Decoding file-resources...
I: Decoding values */* XMLs...
I: Baksmaling classes.dex...
I: Baksmaling classes3.dex...
I: Baksmaling classes2.dex...
I: Copying assets and libs...
I: Copying unknown files...
I: Copying original files...

┌──(adri㉿kali)-[~/picoCTF/Reversing/timer]
└─$ ls  
timer  timer.apk
                                                                                                                                                                                                                                           
┌──(adri㉿kali)-[~/picoCTF/Reversing/timer]
└─$ cd timer

4.-Buscamos la flag en los archivos del analisis

┌──(adri㉿kali)-[~/picoCTF/Reversing/timer/timer]
└─$ grep -r "picoCTF{[^}]*}"
smali_classes3/com/example/timer/BuildConfig.smali:.field public static final VERSION_NAME:Ljava/lang/String; = "picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}"
apktool.yml:  versionName: picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

```

picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}
## Notas adicionales


## Referencias