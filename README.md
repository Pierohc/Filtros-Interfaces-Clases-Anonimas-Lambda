## Filtros:
Creamos una clase llamada Filtro1:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/6ae1ed70-f110-48a5-9571-fbbc05504345)

Luego implementamos el método correspondiente `doFilter` para poder arreglar el error:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/bd821a18-bf5f-4f04-a330-043912c78895)

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/10b6731a-6b44-4548-b8f2-d884f18e8046)

Como doFilter no cuenta con HttpServletRequest, debemos castear al momento de validar la sesion:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/7264e8eb-0460-4008-8c06-ec9ec4c5fd28)

Ahora ya podemos proceder a armar nuestra validación:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/e9800bda-ed3b-4740-b932-dd338d001d5b)


Filter Chain hace que pasemos a la siguiente validación si es que hubiese una:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/24432822-ede9-49e1-8487-01b0a9625252)

Y ya una vez pasando las validaciones, tener que mandarlo al servlet correspondiente:

Agregamos @WebFilter(...) en nuestra clase Filtro1. Cabe resaltar que HttpSession igual se usara en los Servlets, ya sea para obtener o definir atributos:

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/368180ea-f6cd-4b9c-9532-c4ef565bffd4)

![image](https://github.com/Pierohc/Filtros-Interfaces-Clases-Anonimas-Lambda/assets/133154904/472ada37-77fe-45a2-b1e2-57f70e4b0ce1)

Si tenemos varios filtros, como clases Filtro1.java, Filtro2.java, ... , el orden de los filtros en ejecutarse sera por orden alfabético




