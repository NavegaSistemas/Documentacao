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

---

## Trocar senha

> `[POST]` Método utilizado para um usuário trocar a sua senha. O usuário precisa estar logado para realizar esta operação e informar a senha antiga e a nova senha.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/NovaSenha
```

**Exemplo do body da requisição no formato JSON**

```
{
  "login": "00000000000",
  "senhaAtual": "password1",
  "novaSenha": "password2",
}
```

- Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|login|String| CPF do usuário autenticado | S | |
|senhaAtual|String| Senha atual do usuário | S | |
|novaSenha|String| Nova senha do usuário | S | |

---

## Alterar dados do usuário

> `[ POST ]`  Altera os dados de um usuário que esteja logado no aplicativo. 

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/Usuario
```

**Exemplo de body da requisição no formaro JSON**

```
{
	"result": [
    {
      "cpf": "00000000000",
      "email": "seuemail@gmail.com",
      "nome": "Alan Lima",
      "telefone": "99999999999",
      "senha": "",
      "idInstituicao": 0,
      "dataNascimento": "10/03/1997"
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
|senha|String| Senha de acesso do novo usuário |N|A senha deve ser informada como um campo vazio para a alteração de dados de um usuário|
|idInstituicao|Int|Identificador da cooperativa que é usuário já é associado, caso seja. |S|Caso o usuário não seja associado à nenhuma cooperativa, este campo será informado como 0, caso seja a mais de uma, o usuário deve escolher uma de sua preferência |
|dataNascimento|String|Data de nascimento do novo usuário|S|Data deve ser informada no formado dd/mm/yyyy|

---

## Solicita código por e-mail

> `[POST]` Envia um e-mail para o usuário que esqueceu sua senha. Este e-mail irá conter um código de verificação. Este endpoint é usado para recuperação de senha de acesso. **Os dados de autenticação para acessar este endpoint são o usuário e senha padrão da Navega.**

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/EsqueciMinhaSenha?email={email}
```

**Exemplo de resposta**

```
{
  "message": "Código de verificação enviado para e-mail registrado no cadastro do usuário."
}
```

---

## Solicita nova senha

> `[POST]` Para finalizar a recuperação da senha de acesso, deve ser informado a nova senha juntamente com o codigo que foi enviado para o e-mail do usuário. **Os dados de autenticação para acessar este endpoint são o usuário e senha padrão da Navega.** 

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/RecuperaSenha
```

**Exemplo do body da requisição no formato JSON**

```
{
  "email": "seuemail@email.com",
  "codigoVerificacao": 00000,
  "novaSenha": "password",
}
```

- Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|email|String| E-mail que o usuário usou para cadastrar no app | S | |
|codigoVerificacao|Int|Código que é enviado por e-mail para recuperação de senha| S | Este código sempre terá 5 números |
|novaSenha|String| Nova senha informada pelo usuário | S | |

---

## Associa um token ao usuário

> `[POST]` Associa o token do celular de um usuário ao seus dados.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TokenDevice
```

**Exemplo do body da requisição no formato JSON**

```
{
  "login":"02697411607",
  "token": "AKJÇAKJFLKÇAS3165A4F65A4SFAS",
  "os": "Android"
}
```

