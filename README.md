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
| > **docker port id** | Visualizando a porta para acessar da própria máquina|