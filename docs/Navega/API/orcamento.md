## Introdução

O sistema de orçamentos da Navega Consultoria permite que sejam criados
orçamentos para diversos centros de custo e diversas conta contábeis. De forma
a controlar o fluxo de pedidos e compras dentro das Cooperativas de crédito parceiras da empresa.

## Endpoints disponíveis

- [Busca notificações](#busca-notificacoes)
- [Apaga uma notificação](#apaga-uma-notificacao)
- [Notificação como lida](#notificacao-como-lida)

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