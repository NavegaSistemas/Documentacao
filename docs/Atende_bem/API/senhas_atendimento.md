## Cooperativas com senha

> `[ GET ]`  Consulta todas as cooperativas que o usuário logado requisitou alguma senha. É utilizado para ter acesso aos links de cada servidor para uma posterior consulta das senhas de atendimento geradas.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TUnidades/UnidadesSenhas
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idInstituicao": 343,
      "siglaInstituicao": "SICOOB EXECUTIVO",
      "idUnidadeInst": 1,
      "nomeUnidade": "UNIDADE alterado",
      "linkServidorSenhas": "http://cpro29096.publiccloud.com.br:8085",
      "dataHoraEmissao": "12/08/2019 15:23:42"
    }
  ]
}
```