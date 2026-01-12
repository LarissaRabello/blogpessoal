# 📝 Blog Pessoal - API REST com NestJS

<div align="center">
   <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" />
   <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" />
   <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
   <img src="https://img.shields.io/badge/TypeORM-FE0C05?style=for-the-badge&logo=typeorm&logoColor=white" />
</div>

## 💻 Sobre o Projeto

O **Blog Pessoal** é uma API RESTful desenvolvida para gerenciar postagens, temas e usuários de um blog. O projeto foca em boas práticas de desenvolvimento back-end, incluindo autenticação segura, relacionamentos entre entidades e CRUDs completos.

Este projeto foi desenvolvido como parte da minha jornada de estudos em desenvolvimento Fullstack, integrando conhecimentos de segurança e manipulação de dados.

## ⚙️ Funcionalidades

- **Autenticação e Autorização:**
  - [x] Login de Usuário com geração de Token JWT (JSON Web Token).
  - [x] Criptografia de senhas utilizando Bcrypt.
  - [x] Proteção de rotas (Guards).

- **Gestão de Postagens:**
  - [x] Criar, Listar, Atualizar e Deletar postagens.
  - [x] Relacionamento com Temas e Usuários.

- **Gestão de Temas:**
  - [x] Classificação de postagens por temas.

- **Gestão de Usuários:**
  - [x] Cadastro e gerenciamento de perfil de usuário.

## 🛠️ Tecnologias Utilizadas

- **[Node.js](https://nodejs.org/)** - Ambiente de execução.
- **[NestJS](https://nestjs.com/)** - Framework principal.
- **[TypeScript](https://www.typescriptlang.org/)** - Linguagem base.
- **[TypeORM](https://typeorm.io/)** - ORM para comunicação com Banco de Dados.
- **[PostgreSQL](https://www.postgresql.org/)** - Banco de dados relacional (ou MySQL, ajuste conforme seu uso).
- **[Passport](http://www.passportjs.org/) & [JWT](https://jwt.io/)** - Estratégias de autenticação.
- **[Insomnia](https://insomnia.rest/)** - Para testes de requisições API.

## 🚀 Como executar o projeto

### Pré-requisitos
Antes de começar, você precisará ter instalado em sua máquina:
- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en/)
- Um banco de dados configurado (PostgreSQL ou MySQL).

### Instalação

1. Clone o repositório:
```bash
git clone [https://github.com/LarissaRabello/blogpessoal.git](https://github.com/LarissaRabello/blogpessoal.git)
```

2. Acesse a pasta do projeto:Bashcd blogpessoal
Instale as dependências:
```Bash
npm install
```

3. Configure as variáveis de ambiente: Crie um arquivo ```.env``` na raiz do projeto (baseado nas configurações do seu banco) ou configure diretamente no ```app.module.ts``` (para ambiente de dev).

4. Execute a aplicação:
```Bash
# Desenvolvimento
npm run start:dev
```

O servidor iniciará na porta: ```http://localhost:4000``` (ou a porta definida no seu ```main.ts```).

## 🧪 Testando a API
Você pode testar as rotas utilizando o **Thunder Client no VSCode**, **Insomnia** ou **Postman**. Abaixo estão alguns exemplos de endpoints principais:
| Método | Rota | Descrição | Autenticação |
|:---:|:---:|:---|:---:|
| **POST** | `/usuarios/cadastrar` | Cadastra um novo usuário | ❌ Não |
| **POST** | `/usuarios/logar` | Realiza login e retorna Token | ❌ Não |
| **GET** | `/postagens` | Lista todas as postagens | 🔒 Sim |
| **POST** | `/postagens` | Cria uma nova postagem | 🔒 Sim |
| **PUT** | `/postagens` | Atualiza uma postagem | 🔒 Sim |
| **DELETE** | `/postagens/:id` | Deleta uma postagem | 🔒 Sim |
| **GET** | `/temas` | Lista todos os temas | 🔒 Sim |
| **POST** | `/temas` | Cria um novo tema | 🔒 Sim |
