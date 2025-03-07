# ads-senac-2024

<h1>CRUD com Spring Boot: Pessoa e Funcionário</h1>

Descrição
Este projeto demonstra a implementação de um CRUD (Create, Read, Update, Delete) para duas entidades: Pessoa e Funcionario, utilizando Spring Boot e um banco de dados H2.

<h1> Estrutura do Projeto </h1>
src/main/java/
com.example.demo/
controller/ - Controladores REST
model/ - Modelos das entidades Pessoa e Funcionario
repository/ - Repositórios JPA
service/ - Serviços e lógica de negócios
DemoApplication.java - Classe principal
src/main/resources/
application.properties - Configurações do projeto
src/test/java/ - Testes automatizados
Pré-requisitos
Antes de começar, você precisará ter instalado:

Java JDK 11 ou superior
Maven (para gerenciamento de dependências e build)
Instalação

=> Clone o repositório

=> Execute o projeto

O servidor será iniciado em http://localhost:8080.

<h1>Configuração do Banco de Dados</h1>
Este projeto utiliza o banco de dados H2 em memória. A configuração padrão está no arquivo src/main/resources/application.properties:

<h1>properties</h1>
Copiar código
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
Você pode acessar o console do H2 em http://localhost:8080/h2-console com as credenciais:

JDBC URL: jdbc:h2:mem:testdb
User Name: sa
Password: (deixe em branco)

<h1>Estrutura das Entidades</h1>

<h2>Pessoa</h2>

<p>id (Long) - Identificador único</p>
<p>nome (String) - Nome completo</p>
<p>
email (String) - Endereço de e-mail</p>
<p>dataNascimento (LocalDate) - Data de nascimento</p>

<h2>Funcionario</h2>
id (Long) - Identificador único
pessoa (Pessoa) - Referência à entidade Pessoa
cargo (String) - Cargo no qual o funcionário trabalha
salario (BigDecimal) - Salário do funcionário

<h1>Rotas da API</h1>
<h2> Pessoa </h2>
<p>GET /pessoas - Lista todas as pessoas</p>
<p> GET /pessoas/{id} - Retorna uma pessoa específica</p>
<p>  POST /pessoas - Cria uma nova pessoa</p>
<p>PUT /pessoas/{id} - Atualiza uma pessoa existente</p>
<p>DELETE /pessoas/{id} - Remove uma pessoa</p>

<h2>Funcionario</h2>
<p>GET /funcionarios - Lista todos os funcionários</p>
<p>GET /funcionarios/{id} - Retorna um funcionário específico</p>
<p>POST /funcionarios - Cria um novo funcionário</p>
<p>PUT /funcionarios/{id} - Atualiza um funcionário existente</p>
<p>DELETE /funcionarios/{id} - Remove um funcionário</p>






