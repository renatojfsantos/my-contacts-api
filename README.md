# My Contacts API

## Visão Geral

O projeto **MyContacts API** é uma API desenvolvida para gerenciar contatos. Ela permite criar, ler, atualizar e deletar contatos, além de oferecer funcionalidades adicionais para facilitar a gestão de informações de contato.

## Funcionalidades

- **Criação de Contatos**: Permite adicionar novos contatos com informações como nome, email, telefone, etc.
- **Leitura de Contatos**: Permite recuperar a lista de contatos ou detalhes de um contato específico.
- **Atualização de Contatos**: Permite atualizar as informações de um contato existente.
- **Deleção de Contatos**: Permite remover contatos da lista.
- **Busca e Filtros**: Oferece funcionalidades de busca e filtragem para encontrar contatos facilmente.

## Tecnologias Utilizadas

- **Node.js**: Plataforma de desenvolvimento para construir a API.
- **Express.js**: Framework para gerenciar rotas e middlewares.

## Estrutura do Projeto

```
├── src
│   └── app
│   │   ├── controllers
│   │   │   ├── CategoryController.js       # Lida com as requisições relacionadas a categorias
│   │   │   └── ContactController.js        # Lida com as requisições relacionadas a contatos
│   │   ├── middlewares
│   │   │   ├── cors.js                     # Configurações de CORS para a aplicação
│   │   │   └── errorHandler.js             # Middleware para tratamento de erros
│   │   ├── repositories
│   │   │   ├── CategoriesRepository.js     # Gerencia as operações de dados para categorias
│   │   │   └── ContactsRepository.js       # Gerencia as operações de dados para contatos
│   ├── database
│   │   ├── index.js                        # Configuração e inicialização do banco de dados
│   │   └── schema.sql                      # Script SQL para criação do esquema do banco de dados
│   ├── utils
│   │   └── isValidUUID.js                  # Função utilitária para validar UUIDs
│   └── index.js                            # Arquivo principal da aplicação
│   └── routes.js                           # Define as rotas da aplicação
├── .editorconfig                           # Configurações do editor de código
├── .eslintrc.js                            # Configurações do ESLint para padronização de código
├── .gitignore                              # Arquivo para ignorar arquivos no Git
├── package.json                            # Arquivo de manifesto do Node.js
└── README.md                               # Documentação do projeto
```

## Como Executar

### Passo a Passo para Execução

1. **Instale as dependências**:
  ```sh
  npm install
  ```
  ou
  ```sh
  yarn install
  ```

2. **Inicie a aplicação**:
  ```sh
  yarn dev
  ```
  ou
  ```sh
  npm run dev
  ```

  ### Passo a Passo para Executar com Docker

  1. **Certifique-se de ter o Docker instalado**:
    Se você ainda não tem o Docker instalado, siga as instruções no [site oficial do Docker](https://docs.docker.com/get-docker/).

      I. **Crie um container para o PostgreSQL**:
        ```sh
        docker run --name pg -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root -p 5432:5432 -d postgres
        ```

      II. **Inicie o container do PostgreSQL**: Este comando inicia o container do PostgreSQL que foi criado anteriormente.
        ```sh
        docker start pg
        ```

      III. **Verifique os containers em execução**: Este comando lista todos os containers Docker que estão em execução no momento.
        ```sh
        docker ps
        ```

      IV. **Inicie a aplicação**:
        ```sh
        node src/database/index.js
        ```

  2. **Acesse a API**:
    disponível em `http://localhost:3000`.

