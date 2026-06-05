# Documentacion de Contenedores Docker de Sistemas de Datos 
## Contenedor de tutorial de Docker
docker pull docker/getting-started

docker run -d -p 80:80 docker/getting-started

~ -d detach (el proceso del contenedor se ejecuta en background)

~ -p (port, publish)(Mapeo el puerto)

![Imagen Docker](./img/imagen_docker.png)
## Contenedor del SBMS MariaBD 
docker pull mariadb:lts-ubi9

## Contenedor de MariaDB sin volumen
docker run --name ServerMariaDBG2 -e MARIADB_ROOT_PASSWORD=123456 \
-d -p 3345:3306 e0236

## Contenedor de MariaDb con volumen
docker run --name ServerMariaDBG2 -e MARIADB_ROOT_PASSWORD=123456 \
-d -v v-mariadbG2:/var/lib/mysql -p 3345:3306 e0236

## Contenedor de Postgrest con volumen
docker run --name ServerPostgresG2 -e  POSTGRES_PASSWORD=123456 \ -d -p 5457:5432 -v v-postgrestG2:/var/lib/postgresql/data \ eba8d

## Contenedor de SQlServer 2022 con Volumen
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=P@ssw0rd" \
   -u 0 \
   -p 1452:1433 --name SQLServerG2 \
   -d -v vol-sqlserverg2:/var/opt/mssql/data \
   cee0f


/var/lib/mysql

| Comando  | Descripcion |
| :--- | :--- |
| docker pull nombre_imagen  | **Descarga una imagen de DockerHub** [Docker Hub](https://hub.docker.com/)|
| docker images | **Visualizar las imagenes que se encuetran en el docker** |
| docker ps | **Visualizar todos los contenedores que estan encendidos** |
| docker ps -a | **Visualizar todos los contenedores que estan encendidos o y apagados** |
| docker stop idcontenedor o nombre del contenedor | **Detiene un contenedor** |
| docker start idcontenedor o nombre del contenedor | **Enciende un contenedor** |
| docker rm | **Elimina un contenedor si esta apagado** |
| docker rm -f | **Elimina un contenedor este o no encendido** |
