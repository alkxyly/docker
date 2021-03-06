# docker


# **Comandos Docker (Estudos)**


> **docker ps -a** Lista todas as imagens executadas

> **docker ps** Mostra as imagens ativas no momento

> **docker run [nome_imagem]** executa um container

> **docker run it [nome_imagem]** executa de forma iterativa

> **docker stop id** Parar o container de executar

> **docker rm  id** Remove o container do pc

> **docker container prune** Remove todos os container inativos

> **docker images** Mostra todas as imagens 

> **docker rmi [nome_imagem]** Remove uma imagem


| **Commands**  | **Descriptions**  |
|---|---|
| > **docker ps -a**  |  Lista todas as imagens executadas | 
| > **docker run -d dockersamples/static-site** | Executa imagem em background para não travar o terminal|
| > **docker run -d -P dockersamples/static-site** | Docker atribua uma porta aleatória do mundo externo|
| > **docker run -d -P --name meusite dockersamples/static-site** | atribuindo nome a uma imagem|
| > **docker run -d -P -e AUTHOR="XXXXX"  dockersamples/static-site** | atribuindo um valor a variavel de ambiente|
| > **docker port id** | Visualizando a porta para acessar da própria máquina|
| > **docker stop $(docker ps -q)** | Para toda imagem executando a partir dos ids|
| > **docker ps** | exibe todos os containers em execução no momento.|
| > **docker ps -a** | exibe todos os containers, independentemente de estarem em execução ou não.|
| > **docker run -it NOME_DA_IMAGEM** | conecta o terminal que estamos utilizando com o do container.|
| > **docker start ID_CONTAINER** |inicia o container com id em questão|
| > **docker stop ID_CONTAINER** | interrompe o container com id em questão.|
| > **docker start -a -i ID_CONTAINER** | inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.|
| > **docker rm ID_CONTAINER** | remove o container com id em questão.|
| > **docker container prune** | remove todos os containers que estão parados.|
| > **docker rmi NOME_DA_IMAGEM** | remove a imagem passada como parâmetro.|
| > **docker run -d -P --name NOME dockersamples/static-site** | ao executar, dá um nome ao container.|
| > **docker run -d -p 12345:80 dockersamples/static-site** | define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345|
| > **docker run -d -P -e AUTHOR="Fulano" dockersamples/static-site** | define uma variável de ambiente AUTHOR com o valor Fulano no container criado.|
| > **docker run -it -v "C:\Users\assantos\Desktop:/var/www" ubuntu** | relacionando uma pasta local com a pasta do container|
| > **docker run  -p -d 9090:3000 -v "C:\Users\assantos\Desktop\volume-exemplo:/var/www" -w "/var/www"  node npm start** |  Startando uma aplicaçao node dentro de um container|
| > **docker build -f Dockerfile -t douglasq/node .**| Criando uma imagem Dockerfile |
| > **docker run --network minha-rede -d -p 8080:3000 douglasq/alura-books:cap05**| ROdando a aplicacao em uma rede propria|
| > **docker-compose build**| Builda o arquivo docker-compose para baixar todas as imagens necessárias|
| > **docker-compose up**| executa todos os comando do docker compose: abrir porta, subir container|

# Principais comandos utilizados 

## Comandos relacionados às informações

docker version - exibe a versão do docker que está instalada.

docker inspect ID_CONTAINER - retorna diversas informações sobre o container.

docker ps - exibe todos os containers em execução no momento.

docker ps -a - exibe todos os containers, independentemente de estarem em execução ou não.

##  Comandos relacionados à execução

docker run NOME_DA_IMAGEM - cria um container com a respectiva imagem passada como parâmetro.

docker run -it NOME_DA_IMAGEM - conecta o terminal que estamos utilizando com o do container.

docker run -d -P --name NOME dockersamples/static-site - ao executar, dá um nome ao container e define uma porta aleatória.

docker run -d -p 12345:80 dockersamples/static-site - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.

docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM - cria um volume no respectivo caminho do container.

docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM - cria um container especificando seu nome e qual rede deverá ser usada.

## Comandos relacionados à inicialização/interrupção

docker start ID_CONTAINER - inicia o container com id em questão.

docker start -a -i ID_CONTAINER - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.

docker stop ID_CONTAINER - interrompe o container com id em questão.

## Comandos relacionados à remoção

docker rm ID_CONTAINER - remove o container com id em questão.

docker container prune - remove todos os containers que estão parados.

docker rmi NOME_DA_IMAGEM - remove a imagem passada como parâmetro.

## Comandos relacionados à construção de Dockerfile

docker build -f Dockerfile - cria uma imagem a partir de um Dockerfile.

docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM - constrói e nomeia uma imagem não-oficial.

docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM CAMINHO_DOCKERFILE - constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.

## Comandos relacionados ao Docker Hub

docker login - inicia o processo de login no Docker Hub.

docker push NOME_USUARIO/NOME_IMAGEM - envia a imagem criada para o Docker Hub.

docker pull NOME_USUARIO/NOME_IMAGEM - baixa a imagem desejada do Docker Hub.

## Comandos relacionados à rede

hostname -i - mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container).

docker network create --driver bridge NOME_DA_REDE - cria uma rede especificando o driver desejado.

## Comandos relacionados ao docker-compose

docker-compose build - Realiza o build dos serviços relacionados ao arquivo docker-compose.yml, assim como verifica a sua sintaxe.

docker-compose up - Sobe todos os containers relacionados ao docker-compose, desde que o build já tenha sido executado.

docker-compose down - Para todos os serviços em execução que estejam relacionados ao arquivo docker-compose.yml.

docker-compose ps - lista os serviços que estão rodando.

docker exec -it alura-books-1 ping node2 - executa o comando ping node2 dentro do container alura-books-1
