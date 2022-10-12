# EJERCICIO 8

# PASOS A SEGUIR

1) Armamos el archivo docker-compose.

2) Para poder hacer una instancia de nginx que apunte a las dos instancias de passwordapi, realizamos la configuración con el archivo
.conf .

3) Para levantarlo ejecutamos el comando: docker-compose up

4) Verificamos que se levantaron correctamente con el comando: docker ps. Verifico que se crearon los contenedores con los id 3372f92f1e73 para passapi1 y c934012c0ee2 para passapi2

5) Verificamos ejecutando varios requests con el comando : curl --location --request GET 'http://localhost:3000/health'
Ahi vemos que las respuestas tienen como host los id de los contenedores.

host":"3372f92f1e73","loadavg":[0.2138671875,0.6025390625,0.47314453125],"freemem":118919168,"appversion":"2.1.0"}
host":"c934012c0ee2","loadavg":[0.2138671875,0.6025390625,0.47314453125],"freemem":118919168,"appversion":"2.1.0"}

