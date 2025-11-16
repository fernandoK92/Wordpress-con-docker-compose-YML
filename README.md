# Wordpress con docker compose YML
## 1. Título  
Wordpress con docker compose YML

## 2. Tiempo de duración  
25 minutos.  

## 3. Fundamentos  

Docker Compose es una herramienta que permite definir y levantar múltiples contenedores de Docker de manera automática usando un archivo docker-compose.yml.
En esta práctica, se desplegaron:

WordPress → CMS que requiere una base de datos para funcionar.

MySQL → Base de datos relacional para almacenar contenido de WordPress.

phpMyAdmin → Interfaz web para administrar MySQL.

La práctica explora redes internas de contenedores, persistencia de datos con volúmenes y la configuración de entornos de desarrollo reproducibles.

## 4. Conocimientos previos  

Para realizar esta práctica se recomienda conocer:

Conceptos básicos de Docker y contenedores.

Estructura de un archivo docker-compose.yml.

Conceptos de bases de datos relacionales (MySQL, PostgreSQL).

Conceptos de redes y volúmenes en Docker.

Manejo básico de WordPress y phpMyAdmin/pgAdmin.

## 5. Objetivos a alcanzar  

Aprender a desplegar un entorno completo de WordPress con su base de datos y herramientas de administración en contenedores.

Configurar una red interna de contenedores para que los servicios se comuniquen.

Configurar volúmenes para la persistencia de datos de la base de datos.

Conocer cómo levantar, verificar y detener contenedores usando Docker Compose.

Explorar la opción de usar PostgreSQL y pgAdmin para fines de aprendizaje de Docker (aunque WordPress no lo utiliza oficialmente).

## 6. Equipo necesario  

Computadora con sistema operativo Windows, macOS o Linux.

Docker Desktop instalado y funcionando.

Conexión a internet para descargar imágenes oficiales de Docker.

Navegador web para acceder a WordPress y phpMyAdmin/pgAdmin.

## 7. Material de apoyo  

- Documentación de Docker.
- Videos de youtube.
- Documentacui de phpMyAdmin 

## 8. Procedimiento  
wordpress-docker (WordPress + MySQL + phpMyAdmin)

Creamos la carpeta wordpress-docker.

<img width="563" height="97" alt="image" src="https://github.com/user-attachments/assets/735a2577-8e6e-4d97-9cf6-02bd31054bd0" />

Dentro creamos docker-compose.yml con WordPress, MySQL y phpMyAdmin.

<img width="816" height="95" alt="image" src="https://github.com/user-attachments/assets/50b60f98-099f-4923-8c77-1710e8ac9ad2" />

Se nos abrira el bloc de notas y pondremos lo siguiente 

<img width="767" height="852" alt="image" src="https://github.com/user-attachments/assets/69dc3471-4181-4c11-b7b5-3899b4cd9b99" />

Definimos red (wpnet) y volumen (mysqldata) para persistencia.

No olvidar siempre guardar el contenido del bloc de notas con ctrl + s

Ahora Ejecutamos:

docker compose up -d


<img width="1452" height="380" alt="image" src="https://github.com/user-attachments/assets/0183d515-fe3c-4a07-927a-1f1bc71f74df" />


Verificamos con docker ps


<img width="1232" height="98" alt="image" src="https://github.com/user-attachments/assets/06b1467f-4a7e-49a5-aad7-95907f56c1a1" />

Accedemos a WordPress (http://localhost:8080) y phpMyAdmin (http://localhost:8081

 WordPress

 <img width="589" height="310" alt="image" src="https://github.com/user-attachments/assets/7f4db6f6-33f3-4a71-9223-28d7d4db5ed7" />

Configuracion 
 <img width="589" height="316" alt="image" src="https://github.com/user-attachments/assets/eb38d975-76c7-4d69-b767-e6e874301316" />

 
Inicio de WordPress

 <img width="589" height="315" alt="image" src="https://github.com/user-attachments/assets/85b1277b-90c2-46a3-bfef-9984dfc966bf" />

 phpMyAdmin 
 

 <img width="1918" height="1011" alt="image" src="https://github.com/user-attachments/assets/19a8d141-9b9f-4eb3-8949-cbbb361dc342" />

 

 Carpeta wp-postgres (WordPress + PostgreSQL + pgAdmin)

Creamos la carpeta wp-postgres

<img width="423" height="57" alt="image" src="https://github.com/user-attachments/assets/599582ed-bde7-433f-a448-98bc75527551" />


Dentro creamos docker-compose.yml con WordPress, PostgreSQL y pgAdmin.


<img width="502" height="36" alt="image" src="https://github.com/user-attachments/assets/d6bc6b4d-03d3-4e97-b200-8703ac0f9deb" />


Se nos abrira el bloc de notas y pondremos lo siguiente 


<img width="732" height="803" alt="image" src="https://github.com/user-attachments/assets/a57705c5-da6b-4426-9dc6-83d7dbdb357d" />

Definimos red (wpnet) y volúmenes (pgdata y pgadmin_data) para persistencia.

Ejecutamos: docker compose up -d

<img width="1452" height="442" alt="image" src="https://github.com/user-attachments/assets/495c012c-9087-4b06-90d6-548f925c602f" />

Verificamos con docker ps.

<img width="1232" height="147" alt="image" src="https://github.com/user-attachments/assets/19de8da8-4377-4b78-8a57-6b138f88c60f" />


Accedimos a WordPress (http://localhost:8001) y pgAdmin (http://localhost:8081


<img width="589" height="315" alt="image" src="https://github.com/user-attachments/assets/532cdeba-ea75-4d27-a75d-6c4497989aec" />


<img width="1917" height="1048" alt="image" src="https://github.com/user-attachments/assets/fa34ebad-524f-44ed-8349-0b161f447083" />



## 9. Resultados esperados:
Tener 3 contenedores funcionando: WordPress, MySQL y phpMyAdmin.

Poder acceder a WordPress en http://localhost:8080 y verificar su instalación.

Poder acceder a phpMyAdmin en http://localhost:8081 y visualizar la base de datos wpdb.

Que los datos de la base de datos persistan incluso si se reinician los contenedores.

Comprender la estructura de un archivo docker-compose.yml, la definición de redes y volúmenes.

(Extra) Poder levantar WordPress con PostgreSQL y pgAdmin para entender la flexibilidad de Docker.

## 10. Bibliografías
Docker Documentation. Docker Compose Overview. https://docs.docker.com/compose/

WordPress.org. WordPress Installation and Setup. https://wordpress.org/support/

MySQL Documentation. MySQL 5.7 Reference Manual. https://dev.mysql.com/doc/

phpMyAdmin Documentation. https://www.phpmyadmin.net/docs/

pgAdmin Documentation (para práctica extra). https://www.pgadmin.org/docs/
