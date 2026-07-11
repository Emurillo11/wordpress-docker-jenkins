# Despliegue automatizado de WordPress con Docker, Git y Jenkins

## Descripción

Este proyecto implementa un ambiente de WordPress y MySQL utilizando Docker Compose. El proyecto se versiona con Git y GitHub, y Jenkins automatiza el despliegue mediante un Pipeline.

## Tecnologías utilizadas

- Docker
- Docker Compose
- WordPress
- MySQL
- Git
- GitHub
- Jenkins

## Archivos del proyecto

- `.env`: contiene las variables de entorno.
- `docker-compose.yml`: configura WordPress, MySQL, la red y los volúmenes.
- `Jenkinsfile`: contiene el Pipeline de despliegue.
- `README.md`: documenta el funcionamiento del proyecto.

## Contenedores

- `wordpress_app`: ejecuta WordPress.
- `wordpress_db`: ejecuta MySQL 8.0.

## Red personalizada

Los contenedores se comunican mediante la red:

```text
wp-net