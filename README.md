# docker-compose-projeto1-dio
Desafio de Projeto - Criação de um container de uma aplicaçao WEB

O arquivo compose.yaml contém as configurações necessárias para a aplicação WEB utilizando a imagem do apache

Foi utilizado o editor de texto nano para a criação do arquivo .yaml

[compose.yaml](compose.yaml)
```
version: '3.9'
services:
  apache:
    image: httpd:latest
    container_name: my-apache-app
    ports:
    - '80:80'
    volumes:
    - ./website:/usr/local/apache2/htdocs
```

O único serviço utilizando é o apache
Nome do container: my-apache-app
Aplicação estará na pasta chamada website e sendo direcionada dentro da pasta padrão do apache dentro do container

Criando e entrando no diretório website
```
$ mkdir website
$ cd website/
```

Foi utilizado o editor de texto nano para a criação do index.html
```
<html>

<h1> Meu primeiro projeto Docker !!!! </h1>

</html>
```

Instalando o docker compose:
```
$ apt install docker-compose
```

Gerando/subindo o arquivo:
```
$ docker-compose up -d
```
