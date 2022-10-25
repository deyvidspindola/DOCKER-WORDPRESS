# Ambiente Docker Myra Ink

Esse repositório é destinado ao desenvolvimento docker do ambiente do projeto Myra Ink Legacy

## Pré Requisitos
Todo o ambiente foi pensando para rodar um sistema Unix.
Os passos de instalação a seguir foi feito para rodar no Linux.

Para poder configurar o ambiente corretamente certifique-se de ter instalado na maquina as seguintes ferramentas:

* Docker 20.10.14 +
* Makefile (apenas para facilitar a vida, não é obrigatório)

## Configurações na pasta do projeto
Antes de subir o projeto, é necessário dar as permissões para a pasta do projeto. 
```bash
chmod -R 777 app
chown -R www-data app
```

## Subindo o Ambiente
Para subir o ambiente, caso tenha o Makefile instalado basta executar o comando abaixo dentro da pasta do projeto:
```bash
make up
```
Caso não tenho o  Makefile instalado basta executar o comando do docker-compose como descrito abaixo dentro da pasta do projeto:
```bash
docker-compose up -d
```
## Comandos Uteis
Se tiver o Makefile instalado existem alguns comandos para facilitar a usabilidade do genrenciamto do ambiente.

```bash
# subir os container
make up

# baixar os container
make down

# logs dos container
make logs

# bash container nginx
make bash_nginx

# bash container mysql
make bash_mysql

# bash container app
make bash_app
```