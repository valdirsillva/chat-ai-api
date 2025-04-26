# Chat AI API

## Descrição do Projeto

 **Backend** para o aplicativo **Chat AI**, desenvolvido com **Node.js**, **Express** e **TypeScript**.  
 Integra serviços de [**Stream**](https://getstream.io/), [**OpenAI**](https://platform.openai.com/docs/overview) e [**Neon (PostgreSQL)**](https://console.neon.tech/app/projects) usando o ORM **Drizzle**.

O Link para acessar o do frontend Vue.JS [**Aqui**](https://localhost)

## 🧩 Visão Geral

Esta API oferece:

- Cadastro de usuários utilizando a plataforma Stream.

- Criação e gerenciamento de canais de chat em tempo real.

- Integração com OpenAI para geração automática de respostas.

- Armazenamento seguro de históricos de conversas utilizando PostgreSQL.

- ORM moderno e leve (Drizzle) para acesso ao banco de dados.

## 📦 Instalação

1. Clonar o repositório
2. Executar:
   ```bash
    npm install
   ```
5. Crie um .env arquivo no diretório raiz e adicione as seguintes variáveis ​​de ambiente:
 ```bash
    PORT=5000
    STREAM_API_KEY=
    STREAM_API_SECRET=
    OPENAI_API_KEY=
    DATABASE_URL="postgresql://username:password@localhost:5432/dbname"
 ```
4. Execute as migrações:
 ```bash
    npx drizzle-kit generate
    npx drizzle-kit migrate
 ```
5. Inicie o servidor:
 ```bash
  npm run dev
```
## 🌐 Endpoints

- **POST /register-user** - Cria um usuário no chat do Stream e em nosso banco de dados.

- **POST /chat** - Cria um novo canal de chat no Stream, envia uma solicitação ao OpenAI para gerar uma resposta, e salva o histórico no banco de dados.

- **POST /get-messages** - Recupera o histórico de chat de um usuário específico.

## 🚀 Executar em Produção

Este é um projeto TypeScript, portanto, você precisará compilá-lo antes de executá-lo em produção. 
Execute npm run build para compilá-lo. Você poderá então executar o servidor com npm start. 
Os arquivos estarão no dist diretório.
