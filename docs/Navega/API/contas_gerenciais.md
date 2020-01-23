## Introdução

As contas gerenciais são contas que todo Cooperativa de crédito possui. Existem vários grupos em que essas contas são categorizadas e organizadas e a Navega Consultoria analísa todas essas contas e extrai informações úteis para os usuários.


## Endpoints disponíveis

- [Acompanhamento de contas](#acompanhamento-de-contas)
- [Acompanhamento de uma conta](#acompanhamento-de-uma-conta)
- [Painel de contas](#painel-de-contas)
- [Participação diária de unidades](#participa%c3%a7%c3%a3o-di%c3%a1ria-de-unidades)
- [Participação diária de gerentes](#participa%c3%a7%c3%a3o-di%c3%a1ria-de-gerentes)
- [Participação mensal de unidades](#participa%c3%a7%c3%a3o-mensal-de-unidades)
- [Participação mensal de gerentes](#participa%c3%a7%c3%a3o-mensal-de-gerentes)


## Acompanhamento de contas

> `[ GET ]`  Busca acompanhamento de contas, este acompanhamento no app Navega é feito de acordo com as permissões de acesso do usuário. Estas informações são concedidas no ato de login.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/Acompanhe?nivelSaldo={idNivelSaldo}&identificador={idCliente}
```

### Exemplo de resposta
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

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idLogin|Int|Identificador para login do usuário| N | Caso não seja informador irá retornar informações de todos os usuários cadastrados |
|idNivelSaldo|Int|Identificador do nível de saldo que o usuário pode acessar|S|Corresponde ao **IDNivelSaldo** presente na [listagem de um usuário](../usuarios/#busca-de-usuarios)|

---

## Acompanhamento de uma conta

> `[ GET ]` Busca os dados das unidades em relação a um item de acompanhamento de contas.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheItem?idAcompanhe={idAcompanhe}&nivelsaldo={nivelsaldo}
```

### Exemplo de resposta

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

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idAcompanhe|Int|Identificador para a conta selecionada| S | Corresponde ao **IDAcompanhe** presente na [listagem de contas](#acompanhamento-de-contas) |
|nivelsaldo|String|Identificador para o nivel de saldo| N | Possível informar *'gerente'* para dados de gerentes e *'unidade'* para dados das Unidades. Caso um valor não seja informado irá retornar dados das Unidades com default |

---

## Painel de contas

> `[ GET ]` Busca todas as contas do painel gerencial

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/PlanoContas/{id}
```

### Exemplo de resposta

```
{
  "Contas": [
    {
      "IDInstituicao": 475,
      "IDConta": 7000100000000,
      "IDContaReduzido": 70001,
      "IDContaFormatado": "7.0001",
      "IDNivel": 2,
      "DescConta": "Diario",
      "IDGrupo": 7,
      "DescGrupo": "Personalizadas",
      "IDPolaridade": 1,
      "DescPolaridade": "Maior melhor",
      "IDUnidadeMedida": 1,
      "DescUnidadeMedida": "Monet�rio",
      "DescFormato": "R$ #,#0.00",
      "DescSimbolo": "R$",
      "BolDiario": true,
      "BolMensal": true,
      "BolConsolidado": true,
      "BolUnidade": true,
      "BolGerente": true,
      "BolCliente": false
    },
  ]
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|id|Int|Identificador para o grupo de contas| N | Caso não seja informado, irão ser exibidas todas as contas disponíveis. Os id's com seus respesctivos grupos se encontram na [Tabela de grupos de contas](#grupos-de-contas) |

---

## Participação diária de unidades

> `[ GET ]` Busca a participação de todas as unidades de uma cooperativa em relação a uma determinada conta gerencial usando um determinado dia como refêrencia.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/ParticipacaoContaDiaUnidades/{idConta}/{idTipoSaldo}/{data}
```

## Participação diária de gerentes

> `[ GET ]` Busca a participação de todas os gerentes de uma cooperativa em relação a uma determinada conta gerencial usando um determinado dia como refêrencia.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/ParticipacaoContaDiaGerentes/{idConta}/{idTipoSaldo}/{data}
```

## Participação mensal de unidades

> `[ GET ]` Busca a participação de todas as unidades de uma cooperativa em relação a uma determinada conta gerencial usando um determinado mês como refêrencia.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/ParticipacaoContaMesUnidades/{idConta}/{idTipoSaldo}/{data}
```

## Participação mensal de gerentes

> `[ GET ]` Busca a participação de todas os gerentes de uma cooperativa em relação a uma determinada conta gerencial usando um determinado mês como refêrencia.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/ParticipacaoContaMesGerentes/{idConta}/{idTipoSaldo}/{data}
```


### Exemplo de resposta

```
{
  "NivelSaldo": "Unidade",
  "IDContaReduzido": 1,
  "IDTipoSaldo": 1,
  "DescTipoSaldo": "Final",
  "Valores": [
    {
      "ID": 1,
      "IDClienteSisbr": 0,
      "Nome": "UNIDADE 1",
      "TipoPessoa": "-",
      "IDUnidadeInst": 0,
      "IDGerente": 0,
      "NomeUnidade": "-",
      "NomeGerente": "-",
      "DataSaldo": "02/05/2017",
      "Valor": 34994419.04
    },
  ]
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idConta|Int|Identificador para a conta gerencial | S | O ID que deve ser considerado é o "IDContaReduzido" que é obtido através do [endpoint de painel de contas](#painel-de-contas) |
|idTipoSaldo|Int|Identificador do tipo de saldo da conta em questão| S | Os tipos de saldos patrimoniais e de resultado são definidos pelo usuário nas preferências. Caso a conta em questão seja do [grupo](#grupos-de-contas) *Fontes* ou *Usos* o [tipo de saldo](#tipos-de-saldos) será *Final* ou *Médio* (Saldo patrimônial). Caso o [grupo](#grupos-de-contas) seja *Despesas* ou *Receitas* o [tipo de saldo](#tipos-de-saldos) será *Período* ou *Acumulado* (Saldo resultado).|
|data|String|Data de referência para a consulta de participação|S| A data deve ser informada no formato **YYYY-MM-DD**. Para consultas mensais o dia usada é sempre **01**, por exemplo *2018-03-01* para consulta do mês de março.  | 

---

## Informações adicionais

### Grupos de contas

|Id|Grupo|
|--|--|
|1|Fontes/Passivo|
|2|Usos/Ativo|
|3|Despesas|
|4|Receitas|
|5|Corporativo|
|6|Índices|
|7|Personalizadas|

### Tipos de saldos

|Id|Saldo|
|--|--|
|1|Final|
|2|Médio|
|3|Período|
|4|Acumulado|
|5|Corporativo|
|6|Índice|
|7|Personalizado|
