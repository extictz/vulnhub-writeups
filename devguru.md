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






