# backend-alura-instabytes

Este repositório contém a API backend para o projeto Instabytes, desenvolvida com Node.js, Express e MongoDB. O sistema permite o upload de imagens, geração automática de descrições utilizando a API Gemini do Google, e gerenciamento de posts.

## Funcionalidades

- Upload de imagens com armazenamento local.
- Geração automática de descrição (alt-text) para imagens usando IA (Gemini).
- CRUD de posts com MongoDB.

## Estrutura do Projeto
```
.
├──src/
│  ├── config/
│  │   └── dbConfig.js              # Configuração da conexão com o MongoDB
│  ├── controllers/
│  │   └── postsController.js       # Lógica dos endpoints de posts
│  ├── models/
│  │   └── postsModel.js            # Schema e funções do banco de dados
│  ├── routes/
│  │   └── postsRoutes.js           # Definição das rotas da API
│  └── services/
│      └── geminiService.js         # Integração com a API Gemini
├── uploads/                        # Imagens enviadas pelos usuários
└── server.js                       # Inicialização do servidor Express
```
## Requisitos

- Node.js >= 14
- MongoDB Atlas (ou instância local)
- Conta e chave de API Gemini do Google

## Instalação

1. Clone o repositório:
   ```sh
   git clone https://github.com/seu-usuario/backend-alura-instabytes.git
   cd backend-alura-instabytes

2. Instale as dependências:
    ```sh
    npm install

3. Crie um arquivo .env na raiz do projeto com as variáveis: \
    ```sh
    STRING_CONEXAO=<sua-string-de-conexao-mongodb>
    GEMINI_API_KEY=<sua-chave-api-gemini>

4. Inicie o Servidor:
    ```sh
    npm run dev

## Endpoints Principais
GET /posts — Lista todos os posts.\
POST /posts — Cria um novo post.\
POST /upload — Faz upload de uma imagem.\
PUT /upload/:id — Atualiza um post com descrição gerada pela IA.\
### Observações
As imagens são salvas na pasta uploads/.\
O servidor roda por padrão na porta 3000.\
O CORS está liberado para localhost:8000 e 127.0.0.1:8000.\


Desenvolvido para fins educacionais no curso da Alura.
