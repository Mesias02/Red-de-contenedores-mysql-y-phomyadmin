# Red de contenedores mysql y phomyadmin
 

## 1. Título
Implementación de contenedores Docker para MySQL y phpMyAdmin con comunicación en red personalizada.

## 2. Tiempo de duración
160 minutos.

## 3. Fundamentos
Docker es una plataforma de contenedorización que permite empaquetar aplicaciones y servicios con todas sus dependencias. MySQL es un sistema de gestión de bases de datos relacional, mientras que phpMyAdmin es una herramienta basada en web para administrar bases de datos MySQL.
Conceptos claves:
- Docker: Con sus imágenes y contenedores, simplifica la implementación y ejecución de aplicaciones en ambientes consistentes.
- Redes Docker: Las redes personalizadas permiten la conexión entre contenedores para facilitar la comunicación interna.
- MySQL: Su configuración en contenedores involucra definir credenciales de acceso y garantizar la persistencia de datos.
- phpMyAdmin: Su configuración requiere vinculación adecuada al contenedor de MySQL a través de redes.

# Fundamentos
Docker es una plataforma que facilita la creación, despliegue y ejecución de aplicaciones utilizando contenedores. Según la documentación oficial de Docker, "los contenedores son unidades estándar de software que encapsulan código y sus dependencias" (Docker Inc., 2025). Esto garantiza que las aplicaciones sean portables y consistentes en diferentes entornos.
Para configurar redes personalizadas, Docker ofrece comandos que permiten a los contenedores comunicarse eficientemente. Este enfoque asegura una comunicación clara entre servicios, como MySQL y phpMyAdmin, para proyectos como el actual (Docker Inc., 2025).


Docker Logo
Figura 1-1. Ejemplo del ecosistema Docker.

## 4. Conocimientos previos
El estudiante debe conocer:
- Comandos básicos de Docker (ej.: docker run, docker network create, etc.).
- Navegación por interfaces web.
- Configuración básica de bases de datos MySQL.


## 5. Objetivos a alcanzar
- Implementar contenedores para MySQL y phpMyAdmin.
- Configurar una red personalizada que permita la interacción entre ambos contenedores.
- Crear y validar una base de datos de prueba mediante phpMyAdmin.


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
docker run --name mysql --network mi_red_personalizada -e MYSQL_ROOT_PASSWORD=clave -d mysql:latest


Paso 3: Crear contenedor de phpMyAdmin
docker run --name phpmyadmin --network mi_red_personalizada -d phpmyadmin/phpmyadmin


Paso 4: Validar conexión entre contenedores.
Asegúrate de que ambos contenedores están en la misma red usando:
docker network inspect mi_red_personalizada


Figura 1-2. Diagramas de contenedores en la misma red.
Diagrama contenedores

## 9. Resultados esperados
- Pantalla de inicio de phpMyAdmin mostrando conexión exitosa a la base de datos MySQL.
- Base de datos de prueba creada desde la interfaz de phpMyAdmin.


## 10. Bibliografía
Docker Inc. (2025). Docker Documentation. Recuperado de https://docs.docker.com.
