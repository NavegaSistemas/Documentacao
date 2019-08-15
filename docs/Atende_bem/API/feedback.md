## Adiciona um feedback

> `[ PUT ]`  Adiciona um feedback em relação ao aplicativo.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TAjuda/Feedback
```

**Exemplo do body da requisição no formato JSON**

```
{
"texto": "feedback de teste"
}
```

---

## Consulta feedbacks

> `[ GET ]`  Consulta todos os feebacks feitos sobre o aplicativo em um determinado periodo de tempo. Este endpoint é utilizado pela equipe de suporte,

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TAjuda/Feedback?dataInicial={dd/mm/yyyy}&dataFinal={dd/mm/yyyy}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "id": "DDDB37FB-9B5C-4E1A-A62D-DE2BF2ABA472",
      "login": "02697411607",
      "texto": "feedback de teste",
      "datahora": "12/08/2019 18:06:53"
    }
  ]
}
```