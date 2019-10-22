## Unidades 

> `[ GET ]` Busca todas as unidades de uma cooperativa

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/Unidades
```

**Exemplo de resposta**

```
{
  "Unidades": [
    {
      "Codigo": 0,
      "Nome": "UNIDADE 0"
    },
  ]
}
```

---

## Gerentes

> `[ GET ]` Busca todas os gerentes de uma cooperativa

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/Gerentes
```

**Exemplo de resposta**
```
{
  "Gerentes": [
    {
      "Codigo": 1260567,
      "Nome": "ADRIANO SANTOS DA SILVA",
      "Tratamento": "ADRIANO SANTOS",
      "Ativo": true,
      "Unidade": "UNIDADE 0"
    },
  ]
}
```

---

## Regionais

> `[ GET ]` Busca todos os regionais de uma cooperativa

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TCorporativo/Regional
```

**Exemplo de reposta**

```
{
  "Result": [
    {
      "Codigo": 1,
      "Nome": "Regional 1 teste"
    },
  ]
}
```