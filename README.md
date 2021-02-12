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
| > **docker stop $(docker ps -q) ** | Para toda imagem executando a partir dos ids|

| > **docker ps | exibe todos os containers em execução no momento.|
| > **docker ps -a | exibe todos os containers, independentemente de estarem em execução ou não.|
| > **docker run -it NOME_DA_IMAGEM | conecta o terminal que estamos utilizando com o do container.|
| > **docker start ID_CONTAINER |inicia o container com id em questão|
| > **docker stop ID_CONTAINER | interrompe o container com id em questão.|
| > **docker start -a -i ID_CONTAINER | inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.|
| > **docker rm ID_CONTAINER | remove o container com id em questão.|
| > **docker container prune | remove todos os containers que estão parados.|
| > **docker rmi NOME_DA_IMAGEM | remove a imagem passada como parâmetro.|
| > **docker run -d -P --name NOME dockersamples/static-site | ao executar, dá um nome ao container.|
| > **docker run -d -p 12345:80 dockersamples/static-site | define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345|
| > **docker run -d -P -e AUTHOR="Fulano" dockersamples/static-site | define uma variável de ambiente AUTHOR com o valor Fulano no container criado.|