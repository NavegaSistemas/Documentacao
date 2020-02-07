## Introdução

O sistema de orçamentos da Navega Consultoria permite que sejam criados
orçamentos para diversos centros de custo e diversas conta contábeis. De forma
a controlar o fluxo de pedidos e compras dentro das Cooperativas de crédito parceiras da empresa.

## Endpoints disponíveis

- [Orçamentos](#orcamentos)
      - [Listagem de orçamentos](#listagem-de-orcamentos)
      - [Cria um orçamento](#cria-um-orcamento)
- [Produtos](#produtos)
      - [Listagem de produtos](#listagem-de-produtos)
      - [Cria um produto](#cria-um-produto)
      - [Edita um produto](#edita-um-produto)
      - [Excluir um produto](#excluir-um-produto)
- [Fornecedores](#fornecedores)
      - [Listagem de fornecedores](#listagem-de-fornecedores)
      - [Cria um fornecedor](#cria-um-fornecedor)
      - [Edita um fornecedor](#edita-um-fornecedor)
      - [Excluir um fornecedor](#excluir-um-fornecedor)
- [Pedidos](#pedidos)
      - [Listagem de pedidos](#listagem-de-pedidos)
      - [Cria um pedido](#cria-um-pedido)
      - [Aprova/Desaprova um pedido](#aprovadesaprova-um-pedido)
      - [Cancela um pedido](#cancela-um-pedido)
- [Compras](#compras)
      - [Listagem de compras](#listagem-de-compras)
      - [Cria uma compra](#cria-uma-compra)
      - [Recebimento de uma compra](#recebimento-de-uma-compra)
      - [Cancela uma compra](#cancela-uma-compra)
- [Saldo](#saldo)
      - [Listagem de saldo de um orçamento](#listagem-de-saldo-de-um-orcamento)
- [Históricos](#historicos)
      - [Histórico de um pedido](#historico-de-um-pedido)
      - [Histórico de uma compra](#historico-de-uma-compra)

## Orçamentos

Esta é a parte principal deste serviço. É por aqui que o usuário fará o cadastro
do orçamento que servirá como base para todo o controle de fluxo feito pela Navega Sistemas.

### Listagem de orçamentos
``[ GET ]``
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Orcamento
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDOrcamentoGeral": 1,
      "Descricao": "Orcamento 2019",
      "DataInicial": "01/02/2019",
      "DataFinal": "01/01/2020",
      "BolAtivo": true,
      "CentrosCusto": [
        {
          "IDCentroCusto": 3,
          "NomeCentroCusto": "UNIDADE 3",
          "Orcamentos": [
            {
              "NumContaContabil": "8.1.7.06.01.002-1",
              "ValorOrcamento": 200000,
              "NomeContaContabil": "ALUGUEL DE MÓVEIS"
            },
            {
              "NumContaContabil": "8.1.7.36.01.005-3",
              "ValorOrcamento": 100000,
              "NomeContaContabil": "BOLSAS DE ESTUDO"
            }
          ]
        }
      ]
    }
  ]
}
```

### Cria um orçamento
``[ PUT ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Orcamento
```
---
Body
```
{
    "Descricao": "Orcamento 2019",
    "DataInicial": "01/02/2019",
    "DataFinal": "01/01/2020",
    "CentrosCusto": [
        {
            "IDCentroCusto": 3,
			"Orcamentos": [
				{
					"NumContaContabil": "8.1.7.36.01.005-3",
          		    "ValorOrcamento": 100000
				},
				{
					"NumContaContabil": "8.1.7.06.01.002-1",
          		    "ValorOrcamento": 200000
				}
			] 
        }
      ]
    }
```

## Produtos

Os produtos/Serviços que podem ser comprados pelas Cooperativas são previamente cadastrados 
e associados com suas respectivas contas contábeis.

### Listagem de produtos
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Produto
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDProduto": 2,
      "Descricao": "Mesa",
      "NumContaContabil": "8.1.7.06.01.002-1",
      "BolAtivo": false
    },
  ]
}
```


### Cria um produto
``[ PUT ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Produto
```
---
Body
```
{
    "Descricao": "Tesoura",
	"NumContaContabil": "8.1.7.06.01.002-1"
}
```

### Edita um produto
``[ POST ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Produto
```
---
Body
```
{
    "IDProduto": "Tesoura",
	"Descrição": "8.1.7.06.01.002-1"
}
```

### Excluir um produto
``[ DELETE ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Produto?id={}
```

## Fornecedores

Os fornecedores de produtos/serviços das Cooperativas de crédito são cadastrados previamente e devem
ser associado à todas as compras realizadas.

### Listagem de fornecedores
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Fornecedor
```
---
Response
```
{
  "Result": [
    {
      "IDFornecedor": 1,
      "NomeFornecedor": "Maria",
      "NumTelefone": "000000000",
      "Email": "maria@gmail.com",
      "DescEndereco": "Rua X",
      "DescNumero": "508",
      "DescComplemento": "",
      "NomeBairro": "Iporanga",
      "NomeCidade": "Brasilia",
      "NumCEP": "99999999",
      "DataHoraRegistro": "07/02/2020 11:15:47",
      "IDUsuario": 5,
      "BolAtivo": false
    },
  ]
}
```


### Cria um fornecedor
``[ PUT ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Fornecedor
```
---
Body
```
{
	"NomeFornecedor": "Maria",
	"NumTelefone": "000000000",
	"Email": "maria@gmail.com",
	"DescEndereco": "Rua X",
	"DescNumero": "508",
	"DescComplemento": "",
	"NomeBairro": "Iporanga",
	"NomeCidade": "Brasilia",
	"NumCEP": "99999999"
}
```

### Edita um fornecedor
``[ POST ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Fornecedor
```
---
Body
```
{
	"IDFornecedor": 1,
	"NomeFornecedor": "Maria",
	"NumTelefone": "000000000",
	"Email": "maria@gmail.com",
	"DescEndereco": "Rua X",
	"DescNumero": "508",
	"DescComplemento": "",
	"NomeBairro": "Iporanga",
	"NomeCidade": "Brasilia",
	"NumCEP": "99999999"
}
```

### Excluir um fornecedor
``[ DELETE ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Fornecedor?id={}
```

## Pedidos

Após realizar o cadastro do orçamento, dos produtos/serviços e dos fornecedores, o usuário
está apto para realizar as requisições de pedido para que a Navega faça todo o controle
de fluxo necessário. Caso seja realizado um pedido que excede o saldo do orçamento, o mesmo
é encaminhado para o status de "Aguardando aprovação" e algum responsável deve definir se irá 
ou não dar prosseguimento ao pedido.

### Listagem de pedidos
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Pedido?idstatus={}
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDOrcamentoGeral": 1,
      "IDPedido": "0E5CFAEE-C30E-4775-9977-2D18AE60BE56",
      "IDCentroCusto": 3,
      "IDProduto": 2,
      "Descricao": "Mesa",
      "NumContaContabil": "8.1.7.06.01.002-1",
      "Quantidade": 1,
      "DescDetalhamento": "Detalhamento do pedido",
      "DescJustificativa": "Justificativa do pedido",
      "ValorPedido": 200,
      "ValorCompra": 10,
      "IDStatus": 4,
      "DescStatus": "Realizado",
      "DataHoraPedido": "06/02/2020 17:15:34",
      "IDTipoAprovacao": 2,
      "DescricaoTipoAprovacao": "MANUAL"
    },
  ]
}
```

Informações de parâmetros

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idstatus|Int|ID do status do pedido|S|Números inteiros positivos|Os id's valídos com suas respectivas descrições se encontram [AQUI](#status-de-pedidos)|

### Cria um pedido
``[ PUT ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Pedido
```
---
Body
```
{
	"IDOrcamentoGeral": 1,
	"IDCentroCusto": 3,
	"IDProduto": 2,
	"Quantidade": 1,
	"DescDetalhamento": "Detalhamento do pedido",
	"DescJustificativa": "Justificativa do pedido",
	"ValorPedido": 200,
	"BolUrgente": false
}
```

### Aprova/Desaprova um pedido
``[ POST ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Pedido
```
---
Body
```
{
	"IDPedido": "0E5CFAEE-C30E-4775-9977-2D18AE60BE56",
	"Aprovado": true,
	"Observacao": "Observacao de aprovação de pedido"	
}
```

### Cancela um pedido
``[ DELETE ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Pedido?idpedido={}descricao={}
```

## Compras

A compras só podem ser realizadas caso tenha sido feito um pedido anteriormente e o mesmo
tenha sida aprovado (manualmente/automaticamente). Caso o valor da compra seja divergente ao valor
do pedido é utilizado um parâmetro de porcentagem de divergência estabelicido pela Cooperativa. Caso a diferença entre esses valores seja menor que a porcentagem a compra é efetivada, caso contrário é negada.

### Listagem de compras
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Compra?idstatus={}
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDCompra": "50BE4903-F9F9-4140-B056-B891A6FEFD4D",
      "IDPedido": "F8EAEA50-2DC2-4131-8390-968B2D1DCB58",
      "IDFornecedor": 1,
      "NomeFornecedor": "Maria",
      "EmailFornecedor": "maria@gmail.com",
      "TelefoneFornecedor": "000000000",
      "DataCompra": "06/02/2020",
      "ValorCompra": 52,
      "DataPrevisaoEntrega": "10/01/2020",
      "DescObservacao": "Teste de observacao",
      "IDStatusCompra": 3,
      "NumNotaFiscal": "23432423"
    }
  ]
}
```

Informações de parâmetros

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idstatus|Int|ID do status da compra|S|Números inteiros positivos|Os id's valídos com suas respectivas descrições se encontram [AQUI](#status-de-compras)|

### Cria uma compra
``[ PUT ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Compra
```
---
Body
```
{
	"IDPedido": "0E5CFAEE-C30E-4775-9977-2D18AE60BE56",
	"IDFornecedor": 1,
	"ValorCompra": 10,
	"DataPrevisaoEntrega": "10/01/2020",
	"DescObservacao": "Teste de observacao",
	"NumNotaFiscal": "23432423"
}
```

### Recebimento de uma compra
``[ POST ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Compra
```
---
Body
```
{
	"IDCompra": "0E5CFAEE-C30E-4775-9977-2D18AE60BE56"	
}
```

### Cancela uma compra
``[ DELETE ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Compra?idcompra={}observacao={}
```

## Saldo
A consulta de saldos é muito importante para o acompanhamento dos orçamentos que foram
estabelicidos pela Cooperativa. O saldo sofre diferentes ajustes de acordo com a realização
de pedidos, estornos, divergência de valores, etc.

### Listagem de saldo de um orçamento
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/Saldo?idorcamentogeral={}&idcentrocusto&contacontabil={}
```
---
Response
```
{
  "Saldo": 128000,
  "NumContaContabil": "8.1.7.06.01.002-1",
  "IDCentroCusto": 3,
  "IDOrcamentoGeral": 1
}
```

## Históricos
Um pedido e uma compra podem ter seus status alterados até o ponto final do fluxo de cada compra. Por este motivo é importante manter o rastro destes itens para realizar um acompanhamento mais detalhado de todo o orçamento.

### Histórico de um pedido
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/HistoricoPedido?idpedido={}
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDPedido": "72B62785-5FB1-4E83-89F7-78EEB7A9B6CB",
      "DescObservacao": "Entrada de pedido",
      "IDStatus": 1,
      "DescHistorico": "Entrada",
      "DataHoraRegistro": "06/02/2020 17:12:17",
      "IDUsuario": 5,
      "IDLogin": "mob4001_00",
      "NomeTratamento": "João",
      "NomeCompleto": "João da Silva"
    },
  ]
}
```

### Histórico de uma compra
``[ GET ]`` 
```
http://cpro29096.publiccloud.com.br:{PORTA}/navega/api/TOrcamento/HistoricoCompra?idcompra={}
```
---
Response
```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDCompra": "50BE4903-F9F9-4140-B056-B891A6FEFD4D",
      "DescObservacao": "compra cancelada",
      "IDStatusCompra": 3,
      "DescStatus": "Cancelada",
      "DataHoraRegistro": "06/02/2020 18:58:06",
      "IDUsuario": 5,
      "IDLogin": "mob4001_00",
      "NomeTratamento": "João",
      "NomeCompleto": "João da Silva"
    },
  ]
}
```

## Informações adicionais

### Status de pedidos

|ID|Descrição|
|--|--|
|1|Aguardando aprovação|
|2|Aprovado|
|3|Reprovado|
|4|Realizado|
|5|Encerrado|
|6|Cancelado|

### Status de compras

|ID|Descrição|
|--|--|
|1|Realizada|
|2|Recebida|
|3|Cancelada|