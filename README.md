# Docker - Comandos Básicos

## 🔹 Instalação e Verificação
```sh
# Verificar versão do Docker
docker --version

# Verificar se o Docker está em execução
docker info
```

## 🔹 Gerenciamento de Imagens
```sh
# Listar todas as imagens disponíveis
docker images

# Baixar uma imagem do Docker Hub
docker pull <nome_da_imagem>

# Remover uma imagem
docker rmi <id_da_imagem>

# Construir uma imagem a partir de um Dockerfile
docker build -t <nome_da_imagem> .
```

## 🔹 Gerenciamento de Containers
```sh
# Listar containers em execução
docker ps

# Listar todos os containers (incluindo os parados)
docker ps -a

# Iniciar um container
docker start <id_do_container>

# Parar um container
docker stop <id_do_container>

# Remover um container
docker rm <id_do_container>

# Criar e executar um container interativamente
docker run -dit <nome_da_imagem> /bin/bash

# Criar um container e expor uma porta
docker run -d -p 8080:80 <nome_da_imagem>

# Remover todos os containers parados
docker container prune
```

## 🔹 Volumes
```sh
# Criar um volume
docker volume create <nome_do_volume>

# Listar volumes
docker volume ls

# Remover um volume
docker volume rm <nome_do_volume>

# Inspecionar um volume
docker volume inspect <nome_do_volume>
```

## 🔹 Redes
```sh
# Listar redes disponíveis
docker network ls

# Criar uma rede personalizada
docker network create <nome_da_rede>

# Conectar um container a uma rede
docker network connect <nome_da_rede> <id_do_container>

# Desconectar um container de uma rede
docker network disconnect <nome_da_rede> <id_do_container>

# Remover uma rede
docker network rm <nome_da_rede>
```

## 🔹 Docker Compose
```sh
# Subir os serviços definidos no docker-compose.yml
docker-compose up -d

# Parar os serviços
docker-compose down

# Reiniciar os serviços
docker-compose restart

# Verificar logs dos serviços
docker-compose logs -f
```

## 🔹 Outros Comandos Úteis
```sh
# Exibir logs de um container
docker logs <id_do_container>

# Acessar o terminal de um container em execução
docker exec -it <id_do_container> /bin/bash

# Exibir detalhes de um container
docker inspect <id_do_container>

# Parar todos os containers em execução
docker stop $(docker ps -q)

# Remover todas as imagens não utilizadas
docker image prune -a
```

---
