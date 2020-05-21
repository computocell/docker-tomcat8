# Tomcat 8.5.14-alpine

## build
````shell
$ docker build --pull --rm -f "build/Dockerfile" -t computocell/tomcat8.5.14:alpine "build"
````
# Testando conteúdo da imagem

Já com imagem criada vamos iniciar container. Aconselho executar as novas images com a opcão (- -rm) pois o container criado será removido após logout. Como nossa imagem já está funcionando perfeitamente já podemos utilizar o comando abaixo:

````shell
$ docker run -ti -d -p 8080:8080 --name tomcat computocell/tomcat8.5.14:alpine /opt/tomcat/bin/catalina.sh run
````
Como usei a opção -p para expor a porta 8080.