# **API Autobots — Atividade 1**

## Tecnologias Utilizadas:

- Java 17

- Spring Boot 2.6.3

- Spring Web

- Spring Data JPA

- H2 Database

- Lombok

- Maven

---

## Como Executar o Projeto
  
### Pré-requisitos:

- JDK 17 instalado
  
- Maven instalado


### Rodando o projeto:

- mvn spring-boot:run


### A API estará disponível em:

- http://localhost:8080


---

## Rotas relacionadas à **Cliente**:
```
GET /cliente/cliente/{id}
Obter um cliente específico pelo ID.

GET /cliente/clientes/listar
Obter todos os clientes.

POST /cliente/cadastro
Cadastrar um novo cliente.
Recebe no corpo da requisição uma instância de Cliente.

PUT /cliente/atualizar
Atualizar os dados de um cliente existente.
Recebe no corpo da requisição uma instância de Cliente (com 'id').

DELETE /cliente/excluir
Excluir um cliente existente.
Recebe no corpo da requisição uma instância de Cliente (com 'id') a ser excluído.
```

## Rotas relacionadas à **Documento**:

```
GET /documento/documento/{id}
Obter um documento específico pelo ID.

GET /documento/documentos
Obter todos os documentos.

POST /documento/cadastro
Cadastrar um novo documento.
Recebe no corpo da requisição uma instância de documento.

PUT /documento/atualizar
Atualizar os dados de um documento existente.
Recebe no corpo da requisição uma instância de documento (com 'id').

DELETE /documento/excluir
Excluir um documento existente.
Recebe no corpo da requisição uma instância de documento (com 'id') a ser excluído.
```

## Rotas relacionadas à **Endereço**:

```
GET /endereco/endereco/{id}
Obter um endereço específico pelo ID.

GET /endereco/enderecos
Obter todos os endereços.

POST /endereco/cadastro
Cadastrar um novo endereço.
Recebe no corpo da requisição uma instância de endereço.

PUT /endereco/atualizar
Atualizar os dados de um endereço existente.
Recebe no corpo da requisição uma instância de endereço (com 'id').

DELETE /endereco/excluir
Excluir um endereço existente.
Recebe no corpo da requisição uma instância de endereço (com 'id') a ser excluído.
```

## Rotas relacionadas à **Telefone**:

```
GET /telefone/telefone/{id}
Obter um telefone específico pelo ID.

GET /telefone/telefones
Obter todos os telefones.

POST /telefone/cadastro
Cadastrar um novo telefone.
Recebe no corpo da requisição uma instância de Telefone.

PUT /telefone/atualizar
Atualizar os dados de um telefone existente.
Recebe no corpo da requisição uma instância de Telefone (com 'id').

DELETE /telefone/excluir
Excluir um telefone existente.
Recebe no corpo da requisição uma instância de telefone (com 'id') a ser excluído.
```

📋 Modelos de Requisição (Exemplos de JSON)
👤 Cliente
POST /cliente/cadastro

Cadastra um novo cliente.

{
  "nome": "Gabriel Moreira",
  "nomeSocial": "Biel",
  "dataNascimento": "2003-04-10T00:00:00.000+00:00",
  "dataCadastro": "2025-12-01T15:00:00.000+00:00"
}

PUT /cliente/atualizar

Atualiza apenas o nomeSocial do cliente com id: 1.

{
  "id": 1,
  "nomeSocial": "Gabriel M."
}

DELETE /cliente/excluir

Exclui o cliente com id: 1.

{
  "id": 1
}

📄 Documento
POST /documento/cadastro

Cadastra um documento de forma isolada.

{
  "tipo": "CPF",
  "numero": "12345678900"
}

PUT /documento/atualizar

Atualiza o número do documento com id: 2.

{
  "id": 2,
  "numero": "98765432100"
}

DELETE /documento/excluir

Exclui o documento com id: 2.

{
  "id": 2
}

🏠 Endereço
POST /endereco/cadastro

Cadastra um endereço.

{
  "estado": "Minas Gerais",
  "cidade": "Belo Horizonte",
  "bairro": "Savassi",
  "rua": "Rua Pernambuco",
  "numero": "450",
  "codigoPostal": "30130151",
  "informacoesAdicionais": "Apartamento 1203"
}

PUT /endereco/atualizar

Atualiza número e complemento do endereço com id: 2.

{
  "id": 2,
  "numero": "500",
  "informacoesAdicionais": "Próximo ao shopping"
}

DELETE /endereco/excluir

Exclui o endereço com id: 1.

{
  "id": 1
}

📞 Telefone
POST /telefone/cadastro

Cadastra um telefone.

{
  "ddd": "31",
  "numero": "998877665"
}

PUT /telefone/atualizar

Atualiza o número do telefone com id: 2.

{
  "id": 2,
  "numero": "999999999"
}

DELETE /telefone/excluir

Exclui o telefone com id: 2.

{
  "id": 2
}
