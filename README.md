# Projeto Orquestrador do Docker Compose

Este repositório contém a orquestração para o projeto backend-springboot e frontend-angular usando Docker Compose. Para configurar e rodar o projeto, siga os passos abaixo.

## Passos para configurar

1. Clone este repositório:

	git clone https://github.com/letsdevapps/api-creditos-docker-compose.git

2. Entre no projeto criado:

	cd api-creditos-docker-compose

3. Adicione os submódulos do backend e frontend:

	git submodule add https://github.com/letsdevapps/api-creditos-backend-springboot.git backend-springboot

	git submodule add https://github.com/letsdevapps/api-creditos-frontend-angular.git frontend-angular

	git submodule update --init --recursive

4. Agora, você pode construir e iniciar os containers usando o Docker Compose:

	docker-compose up --build

4.1 Caso de erro KeyError: 'ContainerConfig' surja, execute o comando:

	docker-compose down -v --rmi all

	docker-compose up --build

4.2 Caso existam erros, inconsistencias, duplicatas de containers

	docker stop $(docker ps -aq)    # Parar todos os containers

	docker rm $(docker ps -aq)      # Remover todos os containers

	docker rmi $(docker images -q)  # Remover todas as imagens

	docker volume prune -f          # Remover todos os volumes

	docker network prune -f         # Remover redes não usadas
