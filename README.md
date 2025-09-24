# Upload Server

API para upload e gerenciamento de arquivos usando Cloudflare R2 como storage.

## Tecnologias

- Node.js
- TypeScript 
- Fastify
- DrizzleORM
- PostgreSQL
- Cloudflare R2
- Vitest

## Funcionalidades

- Upload de imagens
- Listagem de uploads com filtros
- Exportação de uploads para CSV
- Documentação OpenAPI/Swagger
- Validação com Zod
- Testes automatizados

## Pré-requisitos

- Node.js >= 18
- pnpm
- PostgreSQL
- Conta na Cloudflare R2

## Configuração

1. Clone o repositório
2. Instale as dependências:
```bash
pnpm install
```
## Configure as variáveis de ambiente:
```
PORT=3333

NODE_ENV=development

# Database
DATABASE_URL="postgresql://docker:docker@localhost:5432/upload"

# Cloudflare
CLOUDFLARE_ACCOUNT_ID=""
CLOUDFLARE_ACCESS_KEY_ID=""
CLOUDFLARE_SECRET_ACCESS_KEY=""
CLOUDFLARE_BUCKET=""
CLOUDFLARE_PUBLIC_URL=""
```

## Execute as migrações do banco:

```bash
pnpm db:migrate
```

# Desenvolvimento

Inicie o servidor em modo de desenvolvimento:

```bash
pnpm dev
```

A API estará disponível em 
http://localhost:3333

A documentação Swagger pode ser acessada em http://localhost:3333/docs

# Testes

Execute os testes:
```bash
pnpm test
```

Ou em modo watch:
```bash
pnpm test:watch
```
# Scripts
dev: Inicia o servidor em modo desenvolvimento

test: Executa os testes

test:watch: Executa os testes em modo watch

build: Gera build de produção

db:generate: Gera migrações do banco

db:migrate: Executa migrações do banco

db:studio: Interface visual para o banco

db:migrate:test: Executa migrações no banco de testes



