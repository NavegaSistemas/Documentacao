## Busca categorias de dúvidas

> `[ GET ]` Busca todas as categorias de possíveis dúvidas em relação a vários aspectos do app. (Novidades, fluxo de senhas, etc)
 
```
http://cpro29096.publiccloud.com.br:8084/navega/api/TAjuda/Categorias
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idCategoria": 1,
      "titulo": "Teste",
      "descricao": "Esta é uma categoria de teste"
    }
  ]
}
```

---

## Busca dúvidas de uma categoria

> `[ GET ]` Busca todas as dúvidas contidas em uma categoria
 
```
http://cpro29096.publiccloud.com.br:8084/navega/api/TAjuda/DuvidasCategoria?idCategoria={idCategoria}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idDuvida": 1,
      "titulo": "Pra que serve o app ?",
      "descricao": "O app serve para emitir senhas de atendimento e ser atendido em sua cooperativa"
    }
  ]
}
```

---

## Busca dúvida específica

> `[ GET ]` Busca uma dúvida em específico, utilizando o seu id.
 
```
http://cpro29096.publiccloud.com.br:8084/navega/api/TAjuda/Duvidas?idDuvida=1
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idDuvida": 1,
      "idCategoria": 1,
      "categoria": "Esta é uma categoria de teste",
      "titulo": "Pra que serve o app ?",
      "duvida": "O app serve para emitir senhas de atendimento e ser atendido em sua cooperativa"
    }
  ]
}
```