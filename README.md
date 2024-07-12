# Hello World API

Este é um projeto básico de uma API que responde com "Hello World!" quando acessada. O objetivo é configurar um servidor HTTP simples usando o Express.js.

## Pré-requisitos

- Node.js e npm instalados
- Um editor de texto ou IDE de sua escolha

## Configuração do Ambiente

1. Certifique-se de ter o Node.js e o npm instalados em sua máquina. Você pode verificar se eles estão instalados executando os seguintes comandos no terminal:

    ```bash
    node -v
    npm -v
    ```

   Se não estiverem instalados, você pode baixar e instalar a partir do site oficial do Node.js: [Node.js](https://nodejs.org/).

2. Clone este repositório ou crie um novo diretório para o seu projeto:

    ```bash
    mkdir hello-world-api
    cd hello-world-api
    ```

3. Inicialize um novo projeto Node.js:

    ```bash
    npm init -y
    ```

4. Instale o Express.js:

    ```bash
    npm install express
    ```

## Desenvolvimento

1. Crie um diretório `src` e adicione um arquivo `index.js` com o seguinte conteúdo:

    ```javascript
    // Importa o módulo express
    const express = require('express');

    // Carrega variáveis de ambiente do arquivo .env
    require('dotenv').config();

    // Cria uma nova aplicação express
    const app = express();

    // Define a porta em que o servidor vai escutar a partir das variáveis de ambiente
    const PORT = process.env.PORT || 3000;

    // Define uma rota para o endpoint principal
    app.get('/', (req, res) => {
      res.send('Hello World!');
    });

    // Inicia o servidor e escuta na porta definida
    app.listen(PORT, () => {
      console.log(`Server is running on http://localhost:${PORT}`);
    });
    ```

2. Crie um arquivo `.env` na raiz do projeto e adicione a porta:

    ```dotenv
    PORT=3000
    ```

3. Adicione scripts no `package.json` para iniciar o servidor:

    ```json
    "scripts": {
      "start": "node src/index.js",
      "dev": "nodemon src/index.js"
    }
    ```

4. Para facilitar o desenvolvimento, instale o `nodemon`:

    ```bash
    npm install --save-dev nodemon
    ```

## Executando o Projeto

Para iniciar o servidor em modo de desenvolvimento, execute:

```bash
npm run dev
```

## Testando a API
Abra o seu navegador e vá para http://localhost:3000. Você deve ver a mensagem "Hello World!" exibida.

## Estrutura do Projeto
```
hello-world-api/
├── node_modules/
├── src/
│   └── index.js
├── .env
├── package.json
└── package-lock.json
```

## Contribuição
Sinta-se à vontade para contribuir com este projeto. Você pode abrir issues e pull requests no repositório do GitHub.

## Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para mais detalhes.
```
Este README cobre os principais aspectos do seu projeto, incluindo a configuração do ambiente, desenvolvimento, execução e testes. Você pode ajustar conforme necessário para o seu projeto específico.
```
