## Introdução

As metas são objetivos a serem alcançados pelas Cooperativas de crédito durante um determinado período de tempo. Cada meta 
possui um nome para identificá-la, além de diversos itens, que seriam as metas em si.


## Endpoints disponíveis

- [Busca lista de metas](#busca-lista-de-metas)
- [Busca itens de uma meta](#busca-itens-de-uma-meta)
- [Busca histórico de um item de meta](#busca-historico-de-um-item-de-meta)


## Busca lista de metas
> `[ GET ]` Busca todas as metas com diferentes situações. Estas metas geralmente são cadastradas anualmente pelas cooperativas.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetasSituacao/{idSituacao}
```

### Exemplo de resposta

```
{
  "Metas": [
    {
      "IDInstituicao": 343,
      "IDMeta": 13,
      "DescMeta": "Metas 2019",
      "DataReferencia": "01/03/2017",
      "DataInicial": "01/01/2019",
      "DataFinal": "01/12/2019",
      "IDSituacao": 2,
      "DescSituacao": "Ativa"
    },
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idSituacao|Int|Id da situação da meta| S | Clique [AQUI](#status-de-metas) para visualizar os status de metas disponíveis |

---

## Busca itens de uma meta

> `[ GET ]` Consulta todos os itens de uma determinada meta, estes itens podem ser filtrados por nivel de saldo e periodicidade

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaRealizada?nivelsaldo={nivelSaldo}&identificador={identificador}&periodicidade={periodicidade}&idMeta={idMeta}

```

### Exemplo de resposta

```
{
  "IDInstituicao": 343,
  "IDMeta": 1,
  "DescMeta": "METAS 2016",
  "IDSituacao": 2,
  "DescSituacao": "Ativa",
  "Itens": [
    {
      "IDItem": 1,
      "DescItem": "QUANTIDADE DE ASSOCIADOS",
      "IDPolaridade": 1,
      "DescPolaridade": "Maior melhor",
      "BolConsolidado": true,
      "BolGerente": false,
      "BolUnidade": true,
      "DataSaldo": "01/12/2017",
      "ValorProjetado": 10555,
      "ValorRealizado": 0,
      "PercentualRealizado": 0,
      "IDUnidadeMedida": 2,
      "DescUnidadeMedida": "Quantitativo",
      "Formato": "#,#0"
    },
  ]
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|nivelSaldo|String| nível do saldo da meta| S | **Valores possíveis:** <br> consolidado <br> unidade <br> gerente <br> regional|
|periodicidade|String|periodicidade de acompanhamento da meta| S | **Valores possíveis:** <br> mensal <br> diaria |
|idMeta|Int|id da meta| S | |
|identificador|Int| relacionado ao nível de saldo informado.| S* | Ex.: se o nível de saldo for *unidade*, o identificador é o código da unidade. **< Requerido se nível de saldo diferente de consolidado >**|

---

## Busca histórico de um item de meta

> `[ GET ]` Consulta o histórico de um item de uma meta. Ou seja, caso o nivel de saldo informado seja unidade, irá retornar todas as unidades em relação a um item de uma meta.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaRealizadaItem?nivelsaldo={nivelsaldo}&periodicidade={periodicidade}&idMeta={idMeta}&idItem={idItem}

```

### Exemplo de resposta

```
{
  "IDInstituicao": 343,
  "IDMeta": 1,
  "IDItem": 1,
  "DescItem": "QUANTIDADE DE ASSOCIADOS",
  "IDPolaridade": 1,
  "DescPolaridade": "Maior melhor",
  "BolConsolidado": true,
  "BolGerente": false,
  "BolUnidade": true,
  "IDUnidadeMedida": 2,
  "DescUnidadeMedida": "Quantitativo",
  "Formato": "#,#0",
  "Itens": [
    {
      "ID": 0,
      "Nome": "UNIDADE 0",
      "DataSaldo": "01/12/2017",
      "IDUnidadeInst": 0,
      "ValorProjetado": 5387,
      "ValorRealizado": 0,
      "PercentualRealizado": 0
    },
  ]
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|nivelSaldo|String| nível do saldo da meta| S | **Valores possíveis:** <br> unidade <br> gerente <br> regional|
|periodicidade|String|periodicidade de acompanhamento da meta| S | **Valores possíveis:** <br>mensal <br> diaria|
|idMeta|Int|id da meta| S | |
|idItem|Int| id do item da meta | S |

---

## Informações Adicionais

### Status de metas

|Id|Status|
|--|--|
|1|Cadastro em andamento|
|2|Ativa|
|3|Encerrada|
|4|Cancelada|
|5|Revisada|