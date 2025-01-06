1#Crear archivo dockerfile con instrucciones que necesita nuestro contenedor
para crearse y escribir las configuraciones de nuestro contenedor
2#Crear red interna para que se conecte el backend y el front:network
*para crear*: docker network create *nombre*
*para listar redes*: docker network mired
*para ver*: docker network ls
PARA QUE LAS APLICACIONES SE CONECTEN ENTRE SI
DEBEMOS USAR EL NOMBREID DE CADA CONTENEDOR EN LA CONEXION BACK-FRONT
3#BUILDER APP -t nombreapp:version
docker build -t miapp:1.0.0 .
#COMANDO PARA CREAR EL CONTENEDOR CONECTADO A LA RED --network mired
docker create -p27017:27017 --name mongodb --network mired 
 -e MONGO_INITDB_ROOT_USERNAME=admin MONGO_INITDB_ROOT_PASSWORD=admin mongo