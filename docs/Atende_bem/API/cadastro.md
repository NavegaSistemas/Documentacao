## Verifica associado

> `[ GET ]`  Verifica se uma pessoa ja é associada em alguma ou algumas cooperativas SICOOB. Caso seja associado, retornará dados da cooperativa, caso não seja, retornará um objeto vazio.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/Cliente?cpf={cpf}
```

**Exemplo de resposta**

```
{
  "nomePessoa": "ADENISIO PEREIRA DE LIMA",
  "cooperativas": [
    {
      "idInstituicao": 475,
      "numCooperativa": 4133,
      "siglaInstituicao": "SICOOB SERTÃO"
    },
  ]
}
```


---

## Cadastro

> `[ PUT ]`  Cadastro de um novo usuário no Atende Bem.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/Usuario
```

**Exemplo do body da requisição no formato JSON**

```
{
  result: [
    {
      "cpf": "00000000000",
      "nome": "Seu nome",
      "email": "seuemail@email.com",
      "telefone": "00000000000",
      "senha": "123456",
      "idInstituicao": 143,
      "dataNascimento": "30/09/1997",
    }
  ]
}
```

**Dicionário de dados**

|Chave|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|cpf|String| Identificador de cada pessoa | S | |
|nome|String|Nome completo do usuário| S | |
|email|String| E-mail principal do novo usuário | S | |
|telefone|String| Telefone principal do usuário | N | O DDD deve estar incluso no número de telefone |
|senha|String| Senha de acesso do novo usuário |S||
|idInstituicao|Int|Identificador da cooperativa que é usuário já é associado, caso seja. |S|Caso o usuário não seja associado à nenhuma cooperativa, este campo será informado como 0, caso seja a mais de uma, o usuário deve escolher uma de sua preferência |
|dataNascimento|String|Data de nascimento do novo usuário|S|Data deve ser informada no formado dd/mm/yyyy|

---

## Dados de um usuário

> `[GET]` Usado para realizar o login de um usuário, a identificação do usuário é feita atraves da autenticação feita em Basic Auth. A chave "cooperativas" retornará uma lista de cooperativas que o usuário é associado.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/Usuario
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "login": "00000000000",
      "nome": "Alan lima",
      "email": "Alanronison.lima@gmail.com",
      "dataNascimento": "30/09/1997",
      "telefone": "89767555399",
      "cooperativas": [
        {
          "idInstituicao": 475,
          "numCooperativa": 4133,
          "siglaInstituicao": "SICOOB SERTÃO"
        },
      ]
    }
  ]
}
```
---

## Usuário existe

> `[GET]` Verifica se um determinado usuário já foi cadastrado no aplicativo usando como base o seu cpf.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/UsuarioExiste?cpf={cpf}
```

**Exemplo de resposta**

```
{
  "existe": true
}
```


