[README.md](https://github.com/user-attachments/files/32347327/README.md)
# Api-form-express-mongoDB

API REST para cadastro de usuários (criar, listar, atualizar e remover), construída com **Express** e **Prisma** conectado a um banco **MongoDB**. Projeto de estudo focado em integrar Express com um ORM (Prisma) e um banco não-relacional.

## 🚀 Tecnologias utilizadas

- **Express 5** – servidor HTTP e rotas
- **Prisma** – ORM para acesso ao banco de dados
- **MongoDB** – banco de dados (definido em `prisma/schema.prisma`)

## 📦 Como rodar o projeto

```bash
# clone o repositório
git clone https://github.com/2305ray/Api-form-express-mongoDB.git
cd Api-form-express-mongoDB

# instale as dependências
npm install

# gere o client do Prisma
npx prisma generate

# rode o servidor
node server.js
```

É necessário um banco MongoDB (local ou no MongoDB Atlas) e uma variável de ambiente `DATABASE_URL` com a string de conexão, usada pelo Prisma em `prisma/schema.prisma`. Crie um arquivo `.env` na raiz do projeto:

```
DATABASE_URL="sua-string-de-conexao-mongodb"
```

O servidor sobe na porta `3000`, com as rotas `POST /users`, `GET /users` (aceita filtro por `name` via query string), `PUT /users/:id` e `DELETE /users/:id`.

## 📁 Estrutura

O modelo `User` (`email`, `name`, `age`) é definido em `prisma/schema.prisma`. O client do Prisma é gerado em `generated/prisma`, e toda a lógica das rotas fica em `server.js`.
