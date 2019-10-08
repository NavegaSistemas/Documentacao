# Sobre a API


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

**Relação de portas**
> 8081 > Porta do servidor de testes
> 
> 8082 > Porta do servidor principal para mobile
> 