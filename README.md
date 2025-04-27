# Red de contenedores mysql y phomyadmin
---
 ![image](https://github.com/user-attachments/assets/050164a7-afc9-42cc-ace4-0908076b9806)
---
![image](https://github.com/user-attachments/assets/19c575f9-f665-4922-a8c9-68f78c0143fa)
---

## 1. Título
Implementación de contenedores Docker para MySQL y phpMyAdmin con comunicación en red personalizada.

## 2. Tiempo de duración
160 minutos.

## 3. Desarrollo 
Docker es una plataforma de contenedorización que permite empaquetar aplicaciones y servicios con todas sus dependencias. MySQL es un sistema de gestión de bases de datos relacional, mientras que phpMyAdmin es una herramienta basada en web para administrar bases de datos MySQL.
Conceptos claves:
- Docker: Con sus imágenes y contenedores, simplifica la implementación y ejecución de aplicaciones en ambientes consistentes.
- Redes Docker: Las redes personalizadas permiten la conexión entre contenedores para facilitar la comunicación interna.
- MySQL: Su configuración en contenedores involucra definir credenciales de acceso y garantizar la persistencia de datos.
- phpMyAdmin: Su configuración requiere vinculación adecuada al contenedor de MySQL a través de redes.
----
![image](https://github.com/user-attachments/assets/f9deeb73-3d28-41ec-9df4-0e9a2458adfd)
---
# Fundamentos
Docker es una plataforma que facilita la creación, despliegue y ejecución de aplicaciones utilizando contenedores. Según la documentación oficial de Docker, "los contenedores son unidades estándar de software que encapsulan código y sus dependencias" (Docker Inc., 2025). Esto garantiza que las aplicaciones sean portables y consistentes en diferentes entornos.
Para configurar redes personalizadas, Docker ofrece comandos que permiten a los contenedores comunicarse eficientemente. Este enfoque asegura una comunicación clara entre servicios, como MySQL y phpMyAdmin, para proyectos como el actual (Docker Inc., 2025).


Docker Logo
----
![image](https://github.com/user-attachments/assets/90dcb54f-a067-4a68-9d55-1c644da50c18)
----

## 4. Conocimientos previos
El estudiante debe conocer:
- Comandos básicos de Docker (ej.: docker run, docker network create, etc.).
- Navegación por interfaces web.
- Configuración básica de bases de datos MySQL.


## 5. Objetivos a alcanzar
- Implementar contenedores para MySQL y phpMyAdmin.
---
![image](https://github.com/user-attachments/assets/37c84ed7-9e7f-48cf-982f-763bf0d4ed3a)
---
- Configurar una red personalizada que permita la interacción entre ambos contenedores.
---
![image](https://github.com/user-attachments/assets/306d3f52-8e48-4006-b19c-041b3becd293)
---
- Crear y validar una base de datos de prueba mediante phpMyAdmin.
---
![image](https://github.com/user-attachments/assets/923742ca-79f0-4c52-b073-74b569717878)


## 6. Equipo necesario
- Computador con sistema operativo Windows/Linux/Mac.
- Docker versión 20.10 o superior.
- Acceso a Docker Play (si no se utiliza una instalación local).


## 7. Material de apoyo
- Documentación oficial de Docker.
- Cheat sheet de comandos Linux.
- Guía de asignatura proporcionada por el docente.


## 8. Procedimiento
Paso 1: Crear red personalizada
docker network create mi_red_personalizada


Paso 2: Crear contenedor de MySQL
docker run --name mi_mysql --network mi_red personalizada -e MYSQL_ROOT_PASSWORD=tu_contraseña -e MYSQL_DATABASE=prueba -d mysql:latest
----
![image](https://github.com/user-attachments/assets/e47dd8ce-10f0-4595-9e7a-a8ceaf7402c2)
----
Paso 3: Crear contenedor de phpMyAdmin
docker run --name phpmyadmin --network mi_red_personalizada -d phpmyadmin/phpmyadmin
---
![image](https://github.com/user-attachments/assets/5f1f4ea4-2cf8-4be4-9d95-eb77186820d1)
---
Paso 4: Validar conexión entre contenedores.
----
![image](https://github.com/user-attachments/assets/4df85664-30c0-4f51-ba26-e726b3a5b972)
---


## 9. Resultados esperados
- Pantalla de inicio de phpMyAdmin mostrando conexión exitosa a la base de datos MySQL.
---
![image](https://github.com/user-attachments/assets/26a5ab9d-d3ca-43d0-9d11-4a80155f9e68)
---
- Base de datos de prueba creada desde la interfaz de phpMyAdmin.
---
![image](https://github.com/user-attachments/assets/f884e671-5b15-478b-95f1-0c6612881c61)
---
## 10. Bibliografía
Docker Inc. (2025). Docker Documentation. Recuperado de https://docs.docker.com.
----
Docker, Inc. (n.d.). MySQL Server. Recuperado el 26 de abril de 2025, de https://hub.docker.com/r/mysql/mysql-server/.
----
Geotab, Inc. (n.d.). MyAdmin. Recuperado el 26 de abril de 2025, de https://myadmin.geotab.com/.

