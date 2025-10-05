# Projeto Orquestrador do Docker Compose

Este repositório contém a orquestração para o projeto backend-springboot e frontend-angular usando Docker Compose. Para configurar e rodar o projeto, siga os passos abaixo.

## Passos para configurar

1. Clone este repositório:

   > git clone <URL do repositório de orquestração>
   > cd <nome do repositório>

2. Adicione os submódulos do backend e frontend:

   > git submodule add <URL do repositório backend> backend-springboot
   > git submodule add <URL do repositório frontend> frontend-angular
   > git submodule update --init --recursive

3. Agora, você pode construir e iniciar os containers usando o Docker Compose:

   > docker-compose up --build

3.1 Caso de erro em algo tente apagar arquivos temporarios do diretorio?

   > docker-compose down -v --rmi all
   > docker-compose up --build

