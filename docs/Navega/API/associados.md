## Busca de associados

> `[ GET ]` Busca todos os associados filtrando por nome ou cpf


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/ClientesResumido/{nome_cpf}/{boolean}
```

**Exemplo de resposta**

```
{
  "Clientes": [
    {
      "IDCliente": 1335995,
      "IDOrigem": 1,
      "DescOrigem": "Sisbr",
      "Codigo": 277843,
      "Nome": "ADENISIO PEREIRA DE LIMA",
      "Tratamento": "",
      "CPFCNPJ": "02697411607",
      "TipoPessoa": "PF",
      "Associado": "S",
      "IDUnidade": 0,
      "Unidade": "UNIDADE 0",
      "IDGerente": 1260567,
      "NomeGerente": "ADRIANO SANTOS DA SILVA",
      "NumTelefone": "(61) 996861202"
    },
  ]
}
```


|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|nome_cpf|String|Substituir pelo nome ou cpf do associado|S| Serão considerados trechos de nome que estão entre espaços. Por exemplo, caso o nome seja "Alan Lima", irá ter retorno das informações caso seja informado "Alan" ou "Lima". Uma string "Al" não será suficiente.|
|boolean|String|Caso seja enviado **"true"** (sem aspas), irá retornar os associados de origem SisBr e Navega, caso seja enviado **"false"** (sem aspas) ou **""** (vazio), apenas os de origem SisBr serão listados.|N||



---
 

