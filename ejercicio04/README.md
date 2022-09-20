# Pasos a seguir Ejercicio 4

- Colocar el archivo passwordapi.jar en la carpeta

- Crear el archivo Dockerfile: 

    FROM fabric8/java-alpine-openjdk8-jdk

    COPY ${JAR_FILE} ./app

    EXPOSE 8080

    CMD ["java","-jar","/app/passwordapi.jar"]

- Compilamos con el comando: docker build -f .\Dockerfile  -t zfusari/passwordapi:3.0.0 .

- Corremos la imagen con: docker run --name ejercicio04 -p 3000:3000 zfusari/passwordapi:2.0.0 

- Comprobamos que en http://localhost:3000/ se está corriendo la app

- Subimos la imagen a dockerhub con el comando :  docker push zfusari/passwordapi:3.0.0

- https://hub.docker.com/repository/docker/zfusari/passwordapi
