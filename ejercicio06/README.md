# Pasos a seguir Ejercicio 6

- Agregamos la registry de red hat en el archivo Dockerfile con el 'FROM', encontramos la URL en la documentación.

- Creamos la imagen con el comando: docker build -t passwordapi:6 .

- Corremos la imagen con el comando: docker run -p 3000:3000 passwordapi:6

- Subimos la imagen a dockerhub con el comando: docker image push zfusari/passwordapi:6

- https://hub.docker.com/repository/docker/zfusari/passwordapi
