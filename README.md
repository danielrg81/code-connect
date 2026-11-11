# Code Connect - Monorepo

Workspace configurado com **pnpm workspaces** contendo as seguintes aplicações:

- **`apps/web`**: Aplicação frontend em **React** criada com **Vite** e **TypeScript**.
- **`apps/api`**: Aplicação backend em **NestJS** e **TypeScript**.

---

## 🚀 Como Executar

Instalar dependências de todo o workspace a partir da raiz:
```bash
pnpm install
```

---

## 🛠️ Scripts na Raiz (`package.json`)

Você pode rodar qualquer comando diretamente da raiz sem precisar navegar até os diretórios internos:

### 📦 Workspace Geral
- `pnpm dev` - Inicia ambos os apps (`web` e `api`) em paralelo em modo desenvolvimento.
- `pnpm build` - Compila todos os apps do workspace.
- `pnpm lint` - Executa a verificação de lint em todos os apps.
- `pnpm test` - Executa os testes em todos os apps.

### 🌐 Frontend (React + Vite - `apps/web`)
- `pnpm dev:web` - Inicia o servidor de desenvolvimento do React/Vite.
- `pnpm build:web` - Compila o projeto React para produção.
- `pnpm preview:web` - Visualiza localmente o build de produção.
- `pnpm lint:web` - Executa a verificação de lint no app web.

### ⚙️ Backend (NestJS - `apps/api`)
- `pnpm dev:api` - Inicia a API NestJS em modo watch (`start:dev`).
- `pnpm build:api` - Compila a API NestJS.
- `pnpm start:api` - Inicia a API NestJS normalmente.
- `pnpm start:prod:api` - Inicia o build de produção da API (`node dist/main`).
- `pnpm lint:api` - Executa a verificação de código da API.
- `pnpm test:api` - Executa os testes unitários da API.
- `pnpm test:watch:api` - Executa os testes em modo watch interativo.
- `pnpm test:cov:api` - Gera relatório de cobertura de testes.
- `pnpm test:e2e:api` - Executa os testes de ponta a ponta (e2e).

---

## 📁 Estrutura de Diretórios

```
code-connect/
├── apps/
│   ├── api/             # NestJS App
│   │   ├── src/
│   │   ├── test/
│   │   ├── package.json
│   │   └── ...
│   └── web/             # React + Vite App
│       ├── src/
│       ├── package.json
│       └── ...
├── package.json         # Scripts e atalhos na raiz
├── pnpm-workspace.yaml  # Configuração do pnpm workspace
├── pnpm-lock.yaml
├── .gitignore
└── README.md
```
