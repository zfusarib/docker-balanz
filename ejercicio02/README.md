1) Loguearse en docker hub y crear un repositorio público.
2) Para descargar la imagen: docker pull nicopaez/pingapp:3.0.0 
3) Para loguearse: docker login 
4) Asignarle un tag a la imagen: docker tag nicopaez/pingapp zfusari/balanz-training:ejercicio02
5) Subir imagen a nuestro repositorio de dockerhub: docker push zfusari/balanz-training:ejercicio02
6) Para descargarse la imagen: docker image pull zfusari/balanz-training:ejercicio02