No projeto de hoje, vamos fazer uma API simples usando <strong>NodeJS</strong>.
Essa api vai ser bem simples mas já nos dará uma base bem sólida para alguns conceitos de construção de APIs como rotas, requisições e verbos HTTP.
<strong>E vamos criar tudo passo-a-passo, do absoluto zero!</strong>

Conteúdo do post

Pré-requisitos
Instalando Express
Métodos HTTP
O método GET
Entendendo o req e o res
Retornando JSON
o método POST
A história do Postman
Voltando para requisição POST
O método PUT
O método DELETE
Conclusão
Dever de casa
Pré-Requisitos
Para esse projeto, você precisa do NodeJS instalado em sua máquina, você pode fazer o download e seguir as instruções para o seu sistema operacional diretamente do site deles.

Após fazer a instalação do NodeJS, você deve criar a pasta onde ficará seu projeto. Pelo terminal vá até essa pasta.

Agora vamos criar o arquivo package.json utilizando o seguinte comando:
npm init -y

Pronto! Os pré-requisitos foram cumpridos.

Instalando Express
Agora vamos instalar o Express, que é um framework do NodeJS para criação de aplicações web. Essa instalação é bem simples, basta usar o seguinte comando do NPM:
npm install --save express

Agora que temos o Express instalado, vamos criar um arquivo chamado index.js que será a porta de entrada da nossa aplicação.

No index.js coloque o seguinte conteúdo:

const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => res.send('Minha API'));

app.listen(port, () => console.log(`Listening on port ${port}!`));


Agora vamos rodar esse arquivo, utilizando o comando:
node index.js

Ao executar esse comando, você vai ver um log no terminal dizendo “Listening on port 3000!”, isso significa que o nosso servidor foi inicializado com sucesso e que está pronto para responder requisições no endereço http://localhost:3000 (url localhost, porta 3000).
Agora você pode abrir o seu browser em http://localhost:3000 que o servidor irá responder com o texto “Minha API”
