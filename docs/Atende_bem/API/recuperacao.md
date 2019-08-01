## Solicita código por e-mail

> `[POST]` Envia um e-mail para o usuário que esqueceu sua senha. Este e-mail irá conter um código de verificação.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/EsqueciMinhaSenha?email={email}

```

---

## Solicita nova senha

> `[POST]` http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/RecuperaSenha

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TCadastro/RecuperaSenha
```

- Exemplo do body da requisição abaixo no formato JSON:

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