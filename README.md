# Integración continua con Docker

## Descripción: 
En este proyecto, implementé un flujo de integración continua utilizando Docker para empaquetar y desplegar aplicaciones web desarrolladas en Node.js. Además, utilicé Jenkins como herramienta de automatización para facilitar la construcción y el despliegue continuo.

## Tecnologías utilizadas
- Node.js: Lenguaje de programación para el desarrollo de aplicaciones web.
- Docker: Plataforma de contenedores que permite empaquetar y desplegar aplicaciones de forma sencilla y reproducible.
- Jenkins: Herramienta de automatización que permite la integración continua y el despliegue continuo.

## Funcionalidades
- **Construcción del contenedor Docker** : Configuré un archivo Dockerfile para definir el entorno de ejecución de la aplicación Node.js, incluyendo las dependencias necesarias y la configuración del servidor.
- **Despliegue en diferentes entornos**: Utilicé Docker Compose para definir los servicios y las variables de entorno necesarias para ejecutar la aplicación en diferentes entornos, como desarrollo, pruebas y producción.
- **Pipeline de CI/CD con Jenkins**: Configuré un pipeline de integración continua utilizando Jenkins, que incluyó pasos como la construcción del contenedor Docker, las pruebas automatizadas, la implementación en el entorno de desarrollo y la promoción a los entornos de pruebas y producción.

## Resultados y beneficios

- **Despliegue rápido y eficiente**: Gracias al uso de Docker, el proceso de empaquetar y desplegar la aplicación se simplificó considerablemente, lo que permitió un despliegue rápido y eficiente en diferentes entornos.
- **Mayor confiabilidad y reproducibilidad**: Al utilizar contenedores Docker, garantizamos la consistencia y la reproducibilidad del entorno de ejecución de la aplicación, lo que facilitó la colaboración entre desarrolladores y evitó posibles problemas de configuración.
- **Automatización y ahorro de tiempo**: Jenkins automatizó gran parte del proceso de integración continua y despliegue continuo, lo que redujo la carga de trabajo manual y permitió al equipo enfocarse en otras tareas críticas.

## DOCKER

Comandos

```sh
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:alpine

docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```


docker-compose