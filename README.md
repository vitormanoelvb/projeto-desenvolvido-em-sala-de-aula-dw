<h1 align="center">⚡API CRUD com NestJS + Prisma + SQLite + Insomnia⚡</h1>

Projeto desenvolvido em sala de aula como parte das práticas de **Desenvolvimento Web Backend**, implementando uma API REST simples para o recurso `/usuario`.

A aplicação foi construída com **NestJS + Prisma ORM + SQLite** e testada no **Insomnia**, aplicando corretamente os métodos HTTP e retornando os status adequados.

---

## 🚀 Funcionalidades Implementadas

### 🔹 Métodos HTTP:
- **POST /usuario** → Cria um novo usuário (valida `nome`, `cpf`, `email`, impede duplicados).  
- **GET /usuario** → Lista todos os usuários cadastrados.  
- **PUT /usuario/:id** → Atualiza os dados de um usuário existente (retorna `404` caso não exista).  
- **DELETE /usuario/:id** → Remove um usuário pelo ID.  

### 🔹 Status Codes utilizados:
- `200` → Requisição bem-sucedida.  
- `201` → Registro criado com sucesso.  
- `400` → Erro de validação / dados duplicados.  
- `404` → Registro não encontrado.  

---

## 🛠️ Como Executar o Projeto

### Pré-requisitos:
- Node.js (versão LTS) → [nodejs.org](https://nodejs.org)  
- NestJS CLI instalado globalmente  
  ```bash
  npm i -g @nestjs/cli
  ```
- VS Code com extensões recomendadas:
  - Dracula Official  
  - Material Icon Theme  
  - DotENV  
  - Prisma e Prisma Insider  
  - SQLite + SQLite Viewer  
  - Prettier – Code Formatter  

### Passo a passo:
1. Clone o repositório:
   ```bash
   git clone https://github.com/vitormanoelvb/projeto-desenvolvido-em-sala-de-aula-dw
   cd projeto-desenvolvido-em-sala-de-aula-dw
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Configure o banco de dados SQLite (já existe um `.env` padrão):
   ```env
   DATABASE_URL="file:./dev.db"
   ```
4. Gere o banco e aplique a migration inicial:
   ```bash
   npx prisma migrate dev --name init
   ```
5. Rode o projeto:
   ```bash
   npm run start:dev
   ```
   Servidor disponível em: **http://localhost:3000**

---

## 🔍 Testando a API no Insomnia

Rotas disponíveis:  

### Criar usuário (POST)
```json
{
  "nome": "Ana",
  "cpf": "12345678900",
  "email": "ana@exemplo.com"
}
```

### Listar usuários (GET)
```
GET http://localhost:3000/usuario
```

### Atualizar usuário (PUT)
```json
{
  "nome": "Ana Maria",
  "cpf": "12345678900",
  "email": "ana.maria@exemplo.com"
}
```

### Excluir usuário (DELETE)
```
DELETE http://localhost:3000/usuario/{id}
```

---

## 🖥️ Tecnologias Utilizadas
- **Node.js + NestJS** (backend)  
- **Prisma ORM** (mapeamento e migrations)  
- **SQLite** (banco de dados local)  
- **Insomnia** (testes de API)  
- **VS Code** (IDE)  

---

## 📌 Scripts úteis
```bash
npm run start        # Executar em produção
npm run start:dev    # Executar em desenvolvimento
npm run build        # Compilar o projeto
npm run test         # Executar testes unitários
npm run test:e2e     # Executar testes end-to-end
npx prisma studio    # Abrir interface gráfica do Prisma
```

---

## 🔗 Links Importantes
- 👨‍💻 Autor: [Vitor Manoel Vidal Braz](https://github.com/vitormanoelvb)  
- 📂 Repositório: [Projeto Desenvolvido em Sala - DW](https://github.com/vitormanoelvb/projeto-desenvolvido-em-sala-de-aula-dw)  

---

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Project setup

```bash
$ npm install
```

## Compile and run the project

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Run tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g @nestjs/mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
