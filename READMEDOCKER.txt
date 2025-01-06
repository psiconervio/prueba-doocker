1#Crear archivo dockerfile con instrucciones que necesita nuestro contenedor
para crearse y escribir las configuraciones de nuestro contenedor
2#Crear red interna para que se conecte el backend y el front:network
*para crear*: docker network create *nombre*
*para listar redes*: docker network mired
*para ver*: docker network ls
PARA QUE LAS APLICACIONES SE CONECTEN ENTRE SI
DEBEMOS USAR EL NOMBREID DE CADA CONTENEDOR EN LA CONEXION BACK-FRONT

3#COMANDO PARA CREAR IMAGENES A PARTIR DE UN ARCHIVO DOCKERFILE EN LA RUTA -NOMBRE:-TAG -RUTA
 docker build -t miapp:1 .

4#COMANDO PARA CREAR EL CONTENEDOR CONECTADO A LA RED --network mired
docker create -p27017:27017 --name mongodb --network mired
 -e MONGO_INITDB_ROOT_USERNAME=admin MONGO_INITDB_ROOT_PASSWORD=admin mongo

5#COMANDO PARA CREAR CONTENEDOR DE LA APLICACION QUE CREAMOS EN UNA IMAGEN 3# front -nombre -red -nombreimagen:-tag
docker create -p3000:3000 --name contenedorfront --network mired app:1

#COMANDO PARA VER LAS LOS CONTENEDORES: docker ps -a
#COMANDO PARA INICIAR CONTENEDORES: docker start *nombrecontenedor*