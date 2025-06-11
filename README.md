# 📦 Node.js Backend com Fastify - Upload de Imagens e Exportação CSV

Este é um backend construído com **Node.js** e **Fastify**, projetado para gerenciar o **upload de imagens**, armazenamento no **bucket R2 (Cloudflare)** e exportação dos metadados das imagens em **formato CSV**.

---

## 🚀 Tecnologias Utilizadas

- **[Node.js](https://nodejs.org/)**
- **[Fastify](https://fastify.dev/)** — Framework HTTP leve e de alta performance
- **[Zod](https://zod.dev/)** — Validação de schemas
- **[Swagger (via fastify-swagger)](https://github.com/fastify/fastify-swagger)** — Documentação automática da API
- **[Vitest](https://vitest.dev/)** — Testes unitários
- **[Biome](https://biomejs.dev/)** — Linter e formatter
- **[PostgreSQL](https://www.postgresql.org/)** — Banco de dados relacional
- **[Drizzle ORM](https://orm.drizzle.team/)** — ORM type-safe moderno para TypeScript
- **[Cloudflare R2](https://www.cloudflare.com/products/r2/)** — Armazenamento de objetos compatível com S3
- **[Docker](https://www.docker.com/)** e **[Docker Compose](https://docs.docker.com/compose/)** — Para orquestrar o ambiente do banco de dados
- **[pnpm](https://pnpm.io/)** — Gerenciador de pacotes rápido e eficiente

---

## ✨ Funcionalidades

- 📤 Upload de imagens para o bucket R2
- 🗂️ Armazenamento de metadados das imagens no PostgreSQL
- 📄 Exportação dos dados das imagens em formato CSV
- 📚 Validação dos dados de entrada com Zod
- 🧪 Testes automatizados com Vitest
- 📑 Documentação automática da API com Swagger
- ✅ Linting e formatação padronizados com Biome

---

## 🛠️ Instalação e Execução

### Pré-requisitos

- [Docker](https://www.docker.com/)
- [pnpm](https://pnpm.io/) instalado globalmente

### Passos

```bash
# Clone o repositório
git clone https://github.com/arthurthorp/upload-widget-server
cd nome-do-repo

# Instale as dependências
pnpm install

# Copie o arquivo de variáveis de ambiente
cp .env.example .env
# Edite o .env com suas credenciais (bucket R2, banco de dados, etc.)

# Suba o banco de dados PostgreSQL com Docker Compose
docker-compose up -d

# Rode as migrations com o Drizzle
pnpm run db:migrate

# Inicie o servidor
pnpm dev
```
