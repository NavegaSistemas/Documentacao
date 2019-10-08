## Acompanhamento de contas

> `[ GET ]`  Busca acompanhamento de contas, este acompanhamento no app Navega é feito de acordo com as permissões de acesso do usuário. Estas informações são concedidas no ato de login.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/Acompanhe?nivelSaldo={idNivelSaldo}&identificador={idCliente}
```

**Exemplo de resposta**
```
{
  "Result": [
    {
      "IDAcompanhe": 1,
      "DescAcompanhe": "Saldo Inad01 parcela",
      "DescResumida": "INAD01",
      "IDGrupo": 5,
      "DescGrupo": "Corporativo",
      "IDUnidadeMedida": 1,
      "DescUnidadeMedida": "Monetário",
      "DescSimbolo": "R$",
      "FormatoValor": "R$ #,#0.00",
      "IDPeriodicidade": 1,
      "DescPeriodicidade": "Diário",
      "IDPolaridade": 2,
      "DescPolaridade": "Maior pior",
      "IDTipoGrafico": 1,
      "DescTipoGrafico": "Linhas",
      "IDOrdemExibicao": 1,
      "Valores": [
        {
          "DataSaldo": "20/09/2017",
          "Valor": 1661660.48,
          "VariacaoPercentual": 0,
          "VariacaoBoa": true
        },
        {
          "DataSaldo": "21/09/2017",
          "Valor": 1672233.64,
          "VariacaoPercentual": 0.64,
          "VariacaoBoa": false
        },
        {
          "DataSaldo": "22/09/2017",
          "Valor": 1664467.24,
          "VariacaoPercentual": -0.46,
          "VariacaoBoa": true
        },
        {
          "DataSaldo": "26/09/2017",
          "Valor": 1663489.43,
          "VariacaoPercentual": -0.06,
          "VariacaoBoa": true
        }
      ]
    },
  ]
}
```

**Dicionário de dados**

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idLogin|Int|Identificador para login do usuário| N | Caso não seja informador irá retornar informações de todos os usuários cadastrados |

---

## Acompanhamento de uma conta

> `[ GET ]` Busca os dados das unidades em relação a um item de acompanhamento de contas.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheItem?idAcompanhe={idAcompanhe}
```

**Exemplo de resposta**

```
{
  "Result": [
    {
      "Identificador": 2,
      "Nome": "UNIDADE 2",
      "PosicaoRank": 1,
      "IDAcompanhe": 1,
      "DescAcompanhe": "Saldo Inad01 parcela",
      "Valores": [
        {
          "DataSaldo": "20/09/2017",
          "Valor": 9186.64,
          "VariacaoPercentual": 0,
          "VariacaoBoa": true
        },
        {
          "DataSaldo": "21/09/2017",
          "Valor": 9782.21,
          "VariacaoPercentual": 6.48,
          "VariacaoBoa": false
        },
        {
          "DataSaldo": "22/09/2017",
          "Valor": 9651,
          "VariacaoPercentual": -1.34,
          "VariacaoBoa": true
        },
        {
          "DataSaldo": "26/09/2017",
          "Valor": 9185.66,
          "VariacaoPercentual": -4.82,
          "VariacaoBoa": true
        }
      ]
    },
  ]
}
```

**Dicionário de dados**

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idAcompanhe|Int|Identificador para a conta selecionada| S | |

---
