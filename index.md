# JiraTório
O projeto é uma aplicação web para extração de métricas do jira.

## Precondições para executar o projeto
- Instalar java jdk 8
- Instalar o npm

## Como iniciar o projeto Backend
1- Clone o projeto -> `git clone https://github.com/jirareport/jirareport.git`

2- Criar um banco de dados postgres. 
Para fazer em docker pode executar os seguintes comandos:

- Criar o container:

`docker run --name local-postgres -p 5432:5432 -e POSTGRES_PASSWORD=postgres -d postgres`
(depois da primeira vez, vai precisar executar `docker start local-postgres`)

- Conectar no banco:

`docker run -it --rm --link local-postgres:postgres postgres psql -h postgres -U postgres`

- Criar o esquema:

`create database jirareport;`

3- Copiar o arquivo application.example.yml com o nome application.yml

4- Editar o arquivo application.properties e alterar as propriedades seguintes:
- jira.url: especificar a url do seu jira
- holiday.token: especificar o seu token (Para gerar seu token, possibilitando assim acessar a API de Feriados, basta acessar `http://www.calendario.com.br/api_feriados_municipais_estaduais_nacionais.php` e solicitar seu token por email.)
- spring.datasource.url: caso precisar, altere a url do banco
- spring.datasource.username: caso precisar, alterar o user do banco
- spring.datasource.password: caso precisar, alterar o password do banco

5- Executar o projeto (backend):
- Por linha de comandos, pode rodar o comando `./gradlew bootRun`

6- Executar o projeto front end
- Clone o projeto -> `git clone https://github.com/jirareport/jirareport.git`
- vá a pasta onde houve o clone do projeto e execute o comando npm install
- para rodar a aplicação, use o comando npm start
- irá ser iniciado o projeto no endereço http://localhost:3000



[Configuração inicial](/startConfig.html)
