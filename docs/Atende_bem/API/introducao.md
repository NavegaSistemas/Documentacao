# Sobre a API


A API do Atende bem é de uso restrito. Para ter acesso ao seus recursos é necessário se autenticar. Para isso envie no header de cada requisição uma identificação de usuário no formato de Basic Auth.

Os endpoints que estão relacionados ao cadastro de novos usuários possuem um usuário/senha padrão estabelicido pela Navega. Os demais endpoints usarão o cpf e senha do usuário em questão para acessar os dados.

> Exemplo em JavaScript
```
"headers": {
  'Content-Type': 'application/json',
  'Authorization': "Basic " + base64.encode(`${username}:${password}`)
}
```
