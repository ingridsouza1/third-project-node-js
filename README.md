## Back-end com NodeJS

Nesse user foi desenvolvido um back-end simples que recebe requisiçes HTTP através do http://localhost:3333/ e salva os dados em um array do próprio código.

*para rodar esse projeto, instale as libs com o comando **yarn** e rode o user com o comando **yarn dev***

As requisições aceitas são:

+ **GET** (/users) para **listar** todos os users salvos.

  + A resposta é dada em uma lista de users. Como abaixo:
```JSON
[
  {
    "id": "13d4bdd2-5180-48e1-a0ae-f15642bafb20",
    "name": "Back-end com NodeJS",
    "email": "Rubens Guimarães"
  },
  {
    "id": "9c0274b1-34c3-483d-aba0-4496b40429e9",
    "name": "Front-end com ReactJS",
    "email": "Rubens Guimarães"
  },
  {
    "id": "1c91b467-4bb2-4709-84c1-0977d9d4ce8a",
    "name": "Aplicativo React Native",
    "email": "Rubens Guimarães"
  }
]
```


+ **POST** (/users) para **criar** um novo user.

  + Deve-se enviar os dados no corpo da requisição. Como abaixo:

```JSON
{
	"name": "user 1",
	"email": "Rubens"
}
```

+ **PUT** (/users/valor_do_id) para **editar** um user existente.

  + Deve-se enviar os dados a serem editador no corpo da requisição. Como abaixo:

```JSON
{
	"name": "user 1",
	"owner": "Rubens"
}
```


+ **DELETE** (/users/valor_do_id) para **deletar** um user existente.

  + Nessa requisição não há nada no corpo, apenas o ID como parametro na URL.


* Nesse user também foi desenvolvido uma Middleware para validar o ID do user como UUID quando é feito alguma solicitação com parametro de ID.

