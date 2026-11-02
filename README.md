# Baozi Store API

## Descrição

API REST desenvolvida com Spring Boot para gerenciar clientes, produtos e pedidos de uma loja fictícia de pães chineses.

O projeto foi desenvolvido como atividade prática da disciplina de Desenvolvimento Web Back End, utilizando Java, Spring Boot, Spring Data JPA e MySQL.

## Tecnologias utilizadas

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- MySQL
- Maven
- IntelliJ IDEA
- Postman

## Endpoints da API

A API disponibiliza operações para gerenciar clientes, produtos e pedidos.

### Clientes — `/clientes`

| Método HTTP | Endpoint | Descrição |
|---|---|---|
| POST | `/clientes` | Cadastra um novo cliente |
| GET | `/clientes` | Lista todos os clientes |
| GET | `/clientes/{id}` | Busca um cliente pelo ID |
| DELETE | `/clientes/{id}` | Exclui um cliente pelo ID |

### Produtos — `/produtos`

| Método HTTP | Endpoint | Descrição |
|---|---|---|
| POST | `/produtos` | Cadastra um novo produto |
| GET | `/produtos` | Lista todos os produtos |
| GET | `/produtos/{id}` | Busca um produto pelo ID |
| DELETE | `/produtos/{id}` | Exclui um produto pelo ID |

### Pedidos — `/pedidos`

| Método HTTP | Endpoint | Descrição |
|---|---|---|
| POST | `/pedidos` | Cadastra um novo pedido |
| GET | `/pedidos` | Lista todos os pedidos |
| GET | `/pedidos/{id}` | Busca um pedido pelo ID |
| DELETE | `/pedidos/{id}` | Exclui um pedido pelo ID |



## Pré-requisitos

Para executar o projeto, é necessário ter instalado:

- Java JDK
- Maven
- MySQL Server

## Configuração do banco de dados

Crie um banco de dados MySQL chamado `baozi_store`.

Exemplo de comando SQL:

```sql
CREATE DATABASE baozi_store;
```

Configure as credenciais de acesso ao MySQL no arquivo `application.properties`, localizado em `src/main/resources`.

Exemplo de configuração:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/baozi_store
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

Defina as variáveis de ambiente `DB_USERNAME` e `DB_PASSWORD` com as credenciais do seu banco de dados.

## Executando o projeto

1. Abra o projeto no IntelliJ IDEA.
2. Verifique se o MySQL Server está em execução.
3. Confira as configurações de conexão com o banco de dados.
4. Execute a classe `BaoziStoreApplication`.
5. A API estará disponível em `http://localhost:8080`.
