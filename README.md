# AulaJpa
Olá! Aqui está o README.md para o projeto AulaJpa.

# AulaJpa

Projeto de exemplo para ensinar os conceitos básicos do Spring Data JPA, com o uso de anotações e consultas personalizadas em uma aplicação web Spring Boot.

## Dependências

- Spring Boot 2.5.0
- Spring Data JPA 2.5.0
- H2 Database 1.4.200

## Configuração do banco de dados

O projeto está configurado para usar um banco de dados em memória H2. As propriedades de configuração do banco de dados são definidas no arquivo application.properties.

## Executando o projeto

Para executar o projeto, basta clonar o repositório, abrir o terminal na raiz do projeto e digitar o seguinte comando:

```sh
./mvnw spring-boot:run
```

O projeto será iniciado e estará disponível em http://localhost:8080.

## Endpoints

- GET /users: retorna todos os usuários cadastrados.
- GET /users/page: retorna todos os usuários cadastrados de forma paginada.
- GET /users/search-salary?minSalary={minSalary}&maxSalary={maxSalary}: retorna todos os usuários com salário entre minSalary e maxSalary, de forma paginada.
- GET /users/search-name?name={name}: retorna todos os usuários com nome que contenha a string name, de forma paginada.

## Classes

### UserController

Controller que define os endpoints para o recurso User.

### UserRepository

Interface que estende JpaRepository e define as operações de acesso aos dados para o recurso User.

### User

Entidade que representa a tabela tb_users do banco de dados. Contém as informações dos usuários: id, nome, email e salário.
