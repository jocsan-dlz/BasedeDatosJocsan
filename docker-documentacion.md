# Documentacion de Contenedores Docker de Sistemas de Datos 
## Contenedor de tutorial de Docker
docker pull docker/getting-started

docker run -d -p 80:80 docker/getting-started

~ -d detach (el proceso del contenedor se ejecuta en background)

~ -p (port, publish)(Mapeo el puerto)

![Imagen Docker](./img/imagen_docker.png)
## Contenedor del SBMS MariaBD 
docker pull mariadb:lts-ubi9



| Comando  | Descripcion |
| :--- | :--- |
| docker pull nombre_imagen  | **Descarga una imagen de DockerHub** [Docker Hub](https://hub.docker.com/)|
| docker images | **Visualizar las imagenes que se encuetran en el docker** |
