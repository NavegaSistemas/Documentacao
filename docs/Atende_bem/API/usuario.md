## Trocar senha

> `[POST]` Método utilizado para um usuário trocar a sua senha. O usuário precisa estar logado para realizar esta operação.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/NovaSenha
```

- Exemplo do body da requisição abaixo no formato JSON:

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

> `[ POST ]`  Altera os dados de um usuário. 

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/Usuario
```

---