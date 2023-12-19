# Projeto Node.js com Express

Este é um projeto simples em Node.js utilizando o framework Express para criar um servidor web básico.

## Arquitetura Cliente-Servidor

A web funciona com base no modelo cliente-servidor, onde um cliente solicita recursos e serviços para um servidor. O protocolo principal utilizado é o HTTP. O cliente envia requisições para o servidor, que por sua vez processa essas requisições e retorna as respostas, geralmente em formato de páginas web.

### Cliente

O cliente é responsável por fazer solicitações para o servidor. Normalmente, o cliente é um navegador web, mas também pode ser qualquer aplicativo que faça requisições HTTP.

### Servidor

O servidor é responsável por receber as requisições do cliente e processá-las. Ele envia de volta as respostas, que podem incluir páginas HTML, arquivos CSS, scripts JavaScript, etc.

### Protocolo HTTP

As comunicações entre cliente e servidor são baseadas no protocolo HTTP. As requisições contêm métodos (como GET, POST, etc.) e cabeçalhos, enquanto as respostas incluem status e dados.

## Iniciando o Projeto

Para começar, siga os passos abaixo.

1. Certifique-se de ter o Node.js instalado no seu sistema.

2. Crie um novo diretório para o projeto:

    ```bash
    mkdir meu-projeto
    cd meu-projeto
    ```

3. Inicialize o projeto Node.js:

    ```bash
    npm init -y
    ```

4. Instale o framework Express:

    ```bash
    npm install express
    ```

5. Crie um arquivo JavaScript para o servidor (por exemplo, `app.js`):

    ```javascript
    const express = require('express');
    const app = express();
    const porta = 3000;

    app.get('/', (req, res) => {
      res.send('Olá, mundo!');
    });

    app.listen(porta, () => {
      console.log(`Servidor rodando em http://localhost:${porta}`);
    });
    ```

6. Inicie o servidor:

    ```bash
    node app.js
    ```

7. Abra um navegador e visite http://localhost:3000. Você deverá ver a mensagem "Olá, mundo!".
