# NLW Agents - Server

🚀 API RESTful desenvolvida durante o evento **Next Level Week (NLW)** da **Rocketseat**.

## 🛠️ Tecnologias Utilizadas

### Core

- **[Node.js](https://nodejs.org/)** - Runtime JavaScript
- **[TypeScript](https://www.typescriptlang.org/)** - Superset tipado do JavaScript
- **[Fastify](https://fastify.dev/)** - Framework web high-performance

### Banco de Dados

- **[PostgreSQL](https://www.postgresql.org/)** - Banco de dados relacional
- **[Drizzle ORM](https://orm.drizzle.team/)** - ORM type-safe para TypeScript
- **[pgvector](https://github.com/pgvector/pgvector)** - Extensão para vetores no PostgreSQL

### Validação e Tipagem

- **[Zod](https://zod.dev/)** - Schema validation com TypeScript-first
- **[fastify-type-provider-zod](https://github.com/turkerdev/fastify-type-provider-zod)** - Integração Zod + Fastify

### Qualidade de Código

- **[Biome](https://biomejs.dev/)** - Linter e formatter ultra-rápido
- **[Ultracite](https://github.com/ultracite/ultracite)** - Configuração zero para projetos TypeScript
- **[Husky](https://typicode.github.io/husky/)** - Git hooks
- **[lint-staged](https://github.com/lint-staged/lint-staged)** - Linting em arquivos staged

## 🏗️ Padrões de Projeto

- **API RESTful** - Arquitetura baseada em recursos
- **Type Safety** - Validação completa com TypeScript e Zod
- **Environment Variables** - Configuração via variáveis de ambiente
- **Database Migrations** - Controle de versão do banco com Drizzle
- **Code Quality** - Linting automático e formatação consistente

## 🚀 Setup e Configuração

### Pré-requisitos

- **Node.js** v18+
- **Docker** e **Docker Compose**

### 1. Clonar o repositório

```bash
git clone <repository-url>
cd nlw-agents/server
```

### 2. Instalar dependências

```bash
npm install
```

### 3. Configurar ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3333
DATABASE_URL="postgresql://docker:docker@localhost:5432/agents"
```

### 4. Iniciar banco de dados

```bash
docker-compose up -d
```

### 5. Executar migrations

```bash
npm run db:migrate
```

### 6. Popular banco (opcional)

```bash
npm run db:seed
```

### 7. Iniciar servidor

```bash
# Desenvolvimento (com watch mode)
npm run dev

# Produção
npm start
```

## 📚 Scripts Disponíveis

- `npm run dev` - Inicia servidor em modo desenvolvimento
- `npm start` - Inicia servidor em modo produção
- `npm run db:seed` - Popula banco com dados de exemplo
- `npx ultracite format` - Formata código automaticamente
- `npx ultracite lint` - Executa linting

## 🔌 Endpoints

### Health Check

```
GET /health
```

### Rooms

```
GET /rooms - Lista todas as salas
```

## 🐳 Docker

O projeto utiliza PostgreSQL com a extensão pgvector via Docker Compose para facilitar o desenvolvimento local.

---

Desenvolvido com ❤️ durante o **NLW** da **Rocketseat**
