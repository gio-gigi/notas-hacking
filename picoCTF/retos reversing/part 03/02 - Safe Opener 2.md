# Objetivo
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/291/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
# Pistas
1. Download and try to decompile the file.
# Solución
```
decompilar el archivo .class de java
  import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Base64;
import java.util.Base64.Encoder;

public class SafeOpener {
   public static void main(String[] args) throws IOException {
      BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
      Encoder encoder = Base64.getEncoder();
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
      String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_198203f7}";
      if (password.equals(encodedkey)) {
         System.out.println("Sesame open");
         return true;
      } else {
         System.out.println("Password is incorrect\n");
         return false;
      }
   }
}
                                                                            
┌──(gio㉿kali)-[~/picoctf/reversing/safeopener2]
└─$ cat SafeOpener.class 

┌──(gio㉿kali)-[~/picoctf/reversing/safeopener2]
└─$ strings SafeOpener.class | grep pico
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_198203f7}
                                               

```
# Notas adicionales
# Referencias
- https://www.decompiler.com/jar/7da7f526753c4f7f85d4bc6402046432/SafeOpener.java