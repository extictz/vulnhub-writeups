# 🎯 Informe de Vulneración de la Máquina "BREAKOUT"

# 🚀 Paso 1: Escaneo de Puertos
Realizamos un escaneo de todos los puertos para identificar los servicios activos en la máquina.

![image](https://github.com/user-attachments/assets/ff412655-2084-4cdd-8441-2985d1900256)

![image](https://github.com/user-attachments/assets/b1b128b9-a06f-4da5-b517-38fe08045b19)

# 🌐 Paso 2: Acceso a la Página Web
Accedemos a la página web alojada en la máquina y examinamos el código fuente. Encontramos una clave encriptada al final del código fuente.

![image](https://github.com/user-attachments/assets/ea4d661f-d073-42b3-b331-972ac3af91c0)

🔐 Clave Encriptada:

![image](https://github.com/user-attachments/assets/c828b24e-fc00-4827-a4f8-8c97cf42ebd9)

Desencriptamos la clave usando Brainfuck.

# 🔌 Paso 3: Acceso al Puerto 20000
Accedemos a la web en el puerto 20000 utilizando Firefox.

![image](https://github.com/user-attachments/assets/3924e332-afac-454d-99bf-39ecabbd6d10)

# 👤 Paso 4: Enumeración de Usuarios
Usamos enum4linux para enumerar usuarios y encontramos el usuario cyber.

![image](https://github.com/user-attachments/assets/0bceda66-add5-4628-a1d7-071bdb52fe35)

![image](https://github.com/user-attachments/assets/cfe0d12f-834a-4dc7-93c2-02680e4413ba)

# 🔐 Paso 5: Acceso al Panel de Inicio de Sesión
Ingresamos al panel de inicio de sesión con el usuario cyber y la clave anterior desencriptada.

![image](https://github.com/user-attachments/assets/1b187aa1-0276-4df4-bcc2-042d60207ba3)

# 💻 Paso 6: Command Shell
Buscamos un command shell en la página y listamos los contenidos.

![image](https://github.com/user-attachments/assets/f22875dd-e5ca-47a8-9631-f5097d370225)

# 🔄 Paso 7: Shell Reversa
Ponemos en escucha el puerto 1234 con netcat.

![image](https://github.com/user-attachments/assets/6b47536a-834b-4231-8916-f39b7034f0a1)

Ejecutamos una shell reversa para obtener acceso remoto.

![image](https://github.com/user-attachments/assets/4abe10d3-f1ae-40cc-8d00-bfee8a3a54ed)

# 📂 Paso 8: Exploración del Sistema
Listamos los contenidos y verificamos el sistema operativo.

![image](https://github.com/user-attachments/assets/f0240078-c108-42de-9cf6-bd9b62e29dee)

# 🔍 Paso 9: Búsqueda de Binarios SUID
Buscamos binarios con permisos SUID.

![image](https://github.com/user-attachments/assets/a9dc791e-c27c-4c17-9d09-0196296242bf)

Verificamos los permisos necesarios con getcap.

![image](https://github.com/user-attachments/assets/72269eb1-a854-4acc-9b95-a16037382e0f)

# 📁 Paso 10: Acceso a Backups
Accedemos al directorio de backups y listamos los contenidos.

![image](https://github.com/user-attachments/assets/f64a38aa-5254-43f4-afcd-d0ac8e74359c)

# 📦 Paso 11: Extracción de Contraseña
Movemos el archivo old_pass.bak al directorio actual y lo leemos.

![image](https://github.com/user-attachments/assets/bd990cdb-35af-4d3b-9330-1cc65f5f4112)

Obtenemos la siguiente clave:

![image](https://github.com/user-attachments/assets/745aead0-015d-4d21-87c7-5368299aa8df)

# 🔑 Paso 12: Acceso como Root
Accedemos como usuario root y leemos el archivo rOOt.txt.

![image](https://github.com/user-attachments/assets/d6a0d02e-8f87-4351-afe7-36afd44d0420)

![image](https://github.com/user-attachments/assets/ddbf042b-de80-4d19-b3d1-f5f617a332f6)

Espero que este informe te sea útil y fácil de seguir. ¡Buena suerte! 😊




