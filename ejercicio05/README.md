# HEALTHCHECK 

Con la instrucción HEALTHCHECK podemos decirle a Docker que compruebe periódicamente el estado de salud de nuestro contenedor.
Si todo está OK, devuelve 0 y sino 1. 

# ONBUILD

La instrucción ONBUILD permite especificar un comando para cuando la imágen se use como base para otra compilación.Se ejecutará luego del FROM. Esto es útil si la imagen se usará como base para crear otras imágenes, por ejemplo, un entorno de creación de aplicaciones.

# VOLUME

Esta instrucción hace que todos los container se monten en el directorio especificado con VOLUME. También permite exponer alguna de las diferentes áreas enfocada en el almacenamiento de las bases de datos.