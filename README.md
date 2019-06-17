# Learning Docker

## WADocker
Correr un proyecto J2EE con JDK 8 y Postgres 9.4
### Iniciar manejador de base de datos (Postgres 9.4)
El siguiente comando construye un contenedor tomando como base la imagen **Postgres 9.4**, lo ejecuta en segundo plano y lo elimina cuando el contenedor deje de ejecutarse. Tambien se le asigna un nombre (postgres) al contenedor para posteriormente crear un vinculo hacia este .

    docker run -d --name postgres --rm ivanhdz/wad:proyecto_final-1.0-db_postgres
### Iniciar contenedor para Java Servlets (Tomcat / Jetty)
El siguiente comando utiliza **Tomcat 8 / Jetty 9.4** con jdk 8 para servir como contenedor y, crea un enlace para comunicarse con el contenedor de nombre **postgres**, de esta forma se comunican internamente sin exponer un puerto para el manejador de base de datos
**Tomcat 8:**

     docker run -it --rm --link postgres -p 8888:8080 ivanhdz/wad:proyecto_final-tomcat-1.0
    
**Jetty 9.4:** 

    docker run -it --rm --link postgres -p 8888:8080 ivanhdz/wad:proyecto_final-jetty-1.0

