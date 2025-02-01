# Dockert.List
1. Criacao do Projeto

Criar uma pasta para o projeto:

mkdir todo-list-main-docker && cd todo-list-docker

Criar os arquivos index.html e style.css dentro da pasta todo-list-main-docker.

Criar um Dockerfile para definir a imagem Docker.

2. Criacao do Dockerfile

Criar um arquivo Dockerfile na raiz do projeto com o seguinte conteudo:

# Usa uma imagem base do Nginx
FROM nginx:latest

# Copia os arquivos para a pasta padrao do Nginx
COPY . /usr/share/nginx/html

# Expõe a porta 80 para acesso
EXPOSE 80

3. Construindo a Imagem Docker

Executar o seguinte comando para construir a imagem Docker:

 docker build -t caio310/todo-list-main:1.0.0 .

Substituir meu-usuario pelo seu nome de usuario no Docker Hub.

4. Testando a Imagem Localmente

Rodar um container localmente para testar a aplicacao:

 docker run -d -p 8080:80 meu-usuario/meu-projeto:1.0.0

A aplicacao estara disponivel em: http://localhost:8080

5. Criacao de um Repositorio no GitHub

Criar um repositório no GitHub.

Inicializar o Git no projeto:

git init

Adicionar os arquivos e commitar:

git add .
git commit -m "Versão inicial"

Adicionar o repositório remoto e fazer push:

git remote add origin https://github.com/caio310/todo-list-main-docker.git
git branch -M main
git push -u origin main

6. Publicando a Imagem no Docker Hub

Logar no Docker Hub:

docker login

Enviar a imagem para o Docker Hub:

docker push meu-usuario/meu-projeto:1.0.0

7. Executando a Imagem a Partir do Docker Hub

Em qualquer máquina com Docker instalado, executar:

docker run -d -p 8080:80 caio310/todo-list-main:1.0.0

Agora a aplicacao esta acessivel via http://localhost:8080.

Conclusao

Este README documenta os passos para criar, versionar e publicar uma aplicacao web simples com Docker e Docker Hub.
