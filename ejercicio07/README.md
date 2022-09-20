# Ejercicio 7

# ¿Cuántos contenedores se están ejecutando?

- Ejecutando docker ps podemos ver que se están ejecutando dos contenedores; EJERCICIO07_web_1 y EJERCICIO07_db_1.
En el archivo .yml los vemos como web y db dentro de services.

# ¿Cuales son las imágenes en las que están basados los mencionados contenedores?

- El container EJERCICIO07_web_1 con la imagen nicopaez/jobvacancy-ruby:1.3.0 y el container EJERCICIO07_db_1 con la imagen postgres:14.4-alpine.

# ¿Puedes leer el docker-compose.yml y describir lo que hace cada una de sus lineas?

version: '2' // Indica la version
services:
  web:  // Declara el container web
    image: nicopaez/jobvacancy-ruby:1.3.0 // Le asigna la imagen base 
    links:
      - db // incluye el contenedor db
    ports:
      - "3000:3000" // expone en que puerto se ejecutara
    environment:
      PORT: "3000" // expone en que puerto se ejecutara
      RACK_ENV: "production" // declara que será un ambiente productivo
      DATABASE_URL: "postgres://postgres:Passw0rd!@db:5432/postgres" // declara qué base de datos utilizará
    depends_on:
      - db // realiza una especie de "await" para que corra primero el container db y luego el container web.
  db:
    image: postgres:14.4-alpine // Le asigna la imagen base 
    environment:
      POSTGRES_PASSWORD: Passw0rd! // Declara la variable POSTGRES_PASSWORD para poder utilizar PostgreSQL (lo dice en la documentación)

# Dado que cada contenedor corre en forma aislada ¿Cómo es posible que esos contenedores se vean entre sí?

Para que los contenedores se relacionen el docker compose los coloca en una network. Si no especificamos la network utiliza la network bridge. 
Por lo contrario, si la queremos especificar lo podemos hacer en el archivo .yml .
