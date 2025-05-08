# To-Do List Application

## Descrição

Este é um projeto de aplicação de lista de tarefas (To-Do List) desenvolvido em Java utilizando o framework Spring Boot. A aplicação permite que os usuários gerenciem suas tarefas, incluindo funcionalidades como criação, leitura, atualização e exclusão (CRUD).

## Estrutura do Projeto

A estrutura do projeto segue o padrão MVC (Model-View-Controller):

- **Controller**: Contém os controladores responsáveis por lidar com as requisições HTTP.
  - Local: `src/main/java/br/com/todolist/todolist/controller/`
- **Service**: Contém a lógica de negócios da aplicação.
  - Local: `src/main/java/br/com/todolist/todolist/service/`
- **Repository**: Contém as interfaces para acesso ao banco de dados.
  - Local: `src/main/java/br/com/todolist/todolist/repository/`
- **Entity**: Contém as classes que representam as entidades do banco de dados.
  - Local: `src/main/java/br/com/todolist/todolist/entity/`
- **Resources**: Contém os arquivos de configuração e recursos estáticos.
  - Local: `src/main/resources/`

## Tecnologias Utilizadas

- **Java**: Linguagem de programação principal.
- **Spring Boot**: Framework para simplificar o desenvolvimento de aplicações Java.
- **Maven**: Gerenciador de dependências e automação de build.
- **MySQL**: Banco de dados relacional utilizado para persistência de dados.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

- [Java 17+](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- [Maven](https://maven.apache.org/)

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   ```

2. Navegue até o diretório do projeto:
   ```bash
   cd todolist-java
   ```

3. Execute o projeto utilizando o Maven Wrapper:
   ```bash
   ./mvnw spring-boot:run
   ```
   No Windows, use:
   ```bash
   mvnw.cmd spring-boot:run
   ```

4. Acesse a aplicação no navegador:
   ```
   http://localhost:8080
   ```

## Endpoints Principais

Abaixo estão os principais endpoints disponíveis na aplicação:

- `GET /todos`: Retorna a lista de todas as tarefas.
- `POST /todos`: Cria uma nova tarefa.
- `PUT /todos/{id}`: Atualiza uma tarefa existente.
- `DELETE /todos/{id}`: Exclui uma tarefa.

## Descrição das Entidades

### Todo
A entidade `Todo` representa uma tarefa na aplicação. Ela possui os seguintes atributos:

- **id**: Identificador único da tarefa.
- **nome**: Nome da tarefa.
- **descricao**: Descrição detalhada da tarefa.
- **realizado**: Indica se a tarefa foi concluída (true/false).
- **prioridade**: Nível de prioridade da tarefa (inteiro).

## Configuração do Banco de Dados

1. Certifique-se de que o MySQL está instalado e em execução.
2. Crie um banco de dados para a aplicação:
   ```sql
   CREATE DATABASE todolist;
   ```
3. Configure o arquivo `application.properties` com as credenciais do banco de dados:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/todolist
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
   ```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e enviar pull requests.