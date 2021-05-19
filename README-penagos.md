en el proyecto del api: https://github.com/danielpenagos/api.git

--compilar el proyecto (mvn install), haciendo antes los ajustes en src/main/resources/application.properties
docker build -f Dockerfile.build -t hygieia_api:latest . --progress=plain


Luego en el proyecto principal: https://github.com/danielpenagos/Hygieia.git
para el UI en la carpeta principal, en el UI: 
en el proyecto principal, hacer los ajustes primero en el archivo docker/default.conf y luego compilar el proyecto (mvn install)

docker build -t hygieia_ui:latest . --progress=plain

finalmente en el principal, docker-compose up -d
