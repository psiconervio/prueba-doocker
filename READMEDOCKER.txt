1#Crear archivo dockerfile con instrucciones que necesita nuestro contenedor
para crearse y escribir las configuraciones de nuestro contenedor
2#Crear red interna para que se conecte el backend y el front:network
*para crear*: docker network create *nombre*
*para listar redes*: docker network mired
*para ver*: docker network ls
PARA QUE LAS APLICACIONES SE CONECTEN ENTRE SI
DEBEMOS USAR EL NOMBREID DE CADA CONTENEDOR EN LA CONEXION BACK-FRONT

#MODIFICAR CREDENCIALES DE CONEXION DE BASE DE DATOS A LAS ESTABLECIDAS POR DOCKER Y LA BASE DE DATOS
cambiar
