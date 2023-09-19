# Como criar um servidor com o nodejs




. Abra o terminal, e entre no diretório em que tiver baixado o node

$ cd nome_do_diretório





. Em seguida, ative o node da seguinte forma:

$ source nodeenv-js/bin/activate




(nota: para o próximo passo, caso opite por não utilizar o sudo, no inicio do comando, digite "sudo chown nome_proprietário:nome_grupo index.js")




. Após ativar o node, abra o nano em que estará seu servidor:

$ nano index.js


var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World!');
}).listen(5000);

(observação, substitua o ('Hello World!') pelo conteúdo que deseja para seu servidor, e altere o 5000, que seria a porta de acesso)




. Após modificar o arquivo, clique em ctrl X, S e em seguida em enter, para salvar as alterações, e fechar o nano.

. Para ativar seu servidor, digite:

$ node index.js




. Após ativa-lo, vá em um navegador (certifique-se que seja compatível), e digite o seguinte link, substituindo o 5000, pela porta de acesso que havia escolhido em seu arquivo nano:

http://localhost:5000/
