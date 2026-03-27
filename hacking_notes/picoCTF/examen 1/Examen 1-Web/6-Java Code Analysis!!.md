# Java Code Analysis!!

## Descripción

BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/483/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:58588/).
## Solución

```
{
  "role": "Admin",
  "iss": "bookshelf",
  "exp": 1774403871,
  "iat": 1773799071,
  "userId": 2,
  "email": "admin"
}

contraseña del cifrado: 1234

Great job! Here’s your flag:picoCTF{w34k_jwt_n0t_g00d_42f5774a}
```

picoCTF{w34k_jwt_n0t_g00d_42f5774a}
## Notas adicionales

Nos logeamos como user y nos cambiamos a admin cambiando la cookie cifrada, investigando en el código fuente.
## Referencias

- Para conseguir la cookie admin
	https://jwt.tplant.com.au/