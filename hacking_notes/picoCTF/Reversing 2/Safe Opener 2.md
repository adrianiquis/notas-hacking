# Safe Opener 2

## Descripción

What can you do with this file? I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución

```
1.-Descargamos el archivo y observamos que es un archivo tipo "class" esto significa que es el resultado de una compilación de un archivo java por lo que buscamos una pagina web para decompilarlo

--> https://www.javadecompilers.com/

2.-Descompilamos el archivo y encontramos la flag en el código

    import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Base64;

public class SafeOpener {
   public static void main(String[] args) throws IOException {
      BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
      Base64.Encoder encoder = Base64.getEncoder();
      String encodedkey = "";
      String key = "";

      for(int i = 0; i < 3; ++i) {
         System.out.print("Enter password for the safe: ");
         key = keyboard.readLine();
         encodedkey = encoder.encodeToString(key.getBytes());
         System.out.println(encodedkey);
         boolean isOpen = openSafe(encodedkey);
         if (isOpen) {
            break;
         }

         System.out.println("You have  " + (2 - i) + " attempt(s) left");
      }

   }

   public static boolean openSafe(String password) {
      String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}";
      if (password.equals(encodedkey)) {
         System.out.println("Sesame open");
         return true;
      } else {
         System.out.println("Password is incorrect\n");
         return false;
      }
   }
}
```

picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
## Notas adicionales


## Referencias

https://www.javadecompilers.com/