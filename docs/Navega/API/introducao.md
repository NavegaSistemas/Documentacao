# Sobre a API

## Autenticação

A API da Navega Sistemas é de uso restrito. Para ter acesso ao seus recursos é necessário se autenticar. Para isso envie no header de cada requisição uma identificação de usuário no formato de Basic Auth.

> Exemplo em JavaScript
```
"headers": {
  'Content-Type': 'application/json',
  'Authorization': "Basic " + base64.encode(`${username}:${password}`)
}
```

(*É importante mencionar que os dados que serão retornados serão os relacionados a instituição do usuário logado.*)

---

## Relação de portas

A API Navega usa algumas diferentes portas para diferentes servidores.

|Porta|Servidor|
|--|--|
|8080|Deploy desktop|
|8081|Testes|
|8082|Deploy mobile|

## Verbos

A API utiliza verbos restful. Todos os endpoints retornam status code ``200`` em caso de sucesso.

|Verbo|Descrição|
|--|--|
|``GET``|Seleciona um ou mais itens.|
|``PUT``|Cria um novo item.|
|``POST``|Edita um item.|
|``DELETE``|Deleta um item.|

## Headers Requeridos

|Header|Valor|
|--|--|
|``Content-type``*|``application/json``|
|``Authorization``*|Seu token de acesso ``Basic Auth``|