# 🗄️ Banco de Dados — Sistema de Biblioteca

Projeto de banco de dados desenvolvido em **PostgreSQL**, com o objetivo de praticar criação de tabelas, relacionamentos, chaves primárias, chaves estrangeiras e consultas SQL.

## 🛠️ Tecnologias

* PostgreSQL
* SQL
* pgAdmin 4
* BRModelo

## 📐 Modelagem

### Modelo Conceitual

Representação das entidades e seus relacionamentos.

![Modelo Conceitual](modelagem/modelo_conceitual.png)

### Modelo Lógico

Representação das tabelas, atributos, chaves primárias e chaves estrangeiras.

![Modelo Lógico](modelagem/modelo_logico.png)

## 🗂️ Estrutura do Banco

O banco de dados é composto pelas seguintes tabelas:

### `CLIENTES`

Armazena os dados dos clientes da biblioteca.

Principais campos:

* `cpf` — chave primária
* `nome`
* `datanascimento`
* `telefone`
* `email`

### `LIVROS`

Armazena os livros disponíveis na biblioteca.

Principais campos:

* `id` — chave primária
* `nome`
* `autor`
* `datalancamento`
* `quantidade_cadastrada`

### `EMPRESTIMO`

Registra os empréstimos realizados.

Principais campos:

* `id_emprestimo` — chave primária
* `cpf_cliente` — chave estrangeira
* `id_livro` — chave estrangeira

## 🔗 Relacionamentos

```text
CLIENTES
   │
   │ 1:N
   ▼
EMPRESTIMO
   ▲
   │ N:1
   │
LIVROS
```

A tabela `EMPRESTIMO` u
