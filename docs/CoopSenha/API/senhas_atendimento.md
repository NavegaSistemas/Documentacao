## Cooperativas com senha

> `[ GET ]`  Consulta todas as cooperativas que o usuário logado requisitou alguma senha. É utilizado para ter acesso aos links de cada servidor para uma posterior consulta das senhas de atendimento geradas.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TUnidades/UnidadesSenhas?dataInicial={dd/mm/yyyy}&dataFinal={dd/mm/yyyy}
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

---

## Pedir senha

> `[PUT]` Realiza a requisição de uma senha de atendimento em um determinado ponto de atendimento.Este endpoint será disponibilizado no servidor de cada cooperativa, de forma com que seu IP será usado na url em "linkCooperativa". Os dados de acessos serão os usuários e senhas de autenticação da Navega Consultoria em cada cooperativa.

```
{linkCooperativa}/navega/api/TEmissaoSenha/SenhaApp
```

**Exemplo de body da requisição no formaro JSON**

```
{
  "IDInstituicao": 234,
  "IDUnidadeInst": 2,
  "IDFila": 2,
  "IDDestino": 1,
  "IDTipoIdentificacao": 2,
  "NumDocumento": "00000000000",
  "IDFilaPrincipal": 2,
  "IDDeviceToken": "32423SDFEW353T4GJPI34N43T43T",
  "NumPosicaoNotificacao: "2",
  "latitude": 0.0000,
  "longitude": 0.0000,
}
```

**Dicionário de dados**

|Chave|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|IDInstituicao|Int| Identificador de cada instituição | S | |
|IDUnidadeInst|Int|Identificador de cada unidade de atendimento| S | |
|IDFila|Int| Identificador de cada tipo de fila de atendimento | S | Diz respeito a fila escolhida pelo usuário no ato de solicitação de uma senha. Clique [AQUI](#tipos-de-filas) para visualizar os tipos de filas disponíveis |
|IDDestino|Int| Identificador de cada destino de atendimento | S | Os dados dos destinos de cada unidade estão disponiveis [AQUI](../unidades/#busca-dados-de-uma-unidade). |
|IDTipoIdentificacao|Int| Identifica a origem da senha de atendimento |S| Diz respeito a identificação da origem da senha. Clique [AQUI](#tipos-de-identificacao) para visualizar os tipos de identificação disponíveis. |
|NumDocumento|String| Número de CPF do usuário |S| |
|IDFilaPrincipal|Int|Identificador do tipo de usuário|S| Objetivo de saber se o usuário que solicitou a senha é associado ou não da cooperativa. Seja, **2** para ASSOCIADO e **3** para NÃO ASSOCIADO. |
|IDDeviceToken|String| Token do celular do usuário |S| |
|NumPosicaoNotificacao|Int| Parâmetro para envio de push notifications referente a quantidade de pessoas na frente do usuário que emitiu uma senha de atendimento |S| |
|latitude|Float| Latitude do usuário ao emitir uma senha de atendimento |S| |
|longitude|Float| Longitude do usuário ao emitir uma senha de atendimento |S| |

---

## Pessoas na fila

> `[ GET ]`  Consultas quantas pessoas estão na frente de determinada senha de atendimento em um ponto de atendimento específico. Este endpoint será disponibilizado no servidor de cada cooperativa, de forma com que seu IP será usado na url em "linkCooperativa". Os dados de acessos serão os usuários e senhas de autenticação da Navega Consultoria em cada cooperativa.

```
{linkCooperativa}/navega/api/TEmissaoSenha/PessoasNaFrente?idInstituicao={idInstituicao}&idAtendimento={idAtendimento}
```

**Exemplo de resposta**

```
{
  "IDAtendimento": 175398,
  "PessoasNaFrente": 0
}
```

---

## Busca senhas

> `[ GET ]`  Busca senhas de atendimento que foram solicitadas pelo usuário logado em determinado ponto de atendimento. Este endpoint será disponibilizado no servidor de cada cooperativa, de forma com que seu IP será usado na url em "linkCooperativa". Os dados de acessos serão os usuários e senhas de autenticação da Navega Consultoria em cada cooperativa.

```
{linkcooperativa}/navega/api/TEmissaoSenha/SenhasAplicativo?idInstituicao={idInstituicao}&cpf={cpf}
```

* Parâmetros disponíveis

|Parametro|Descrição|Requerido|Valores possíveis|
|--|--|--|--|
|idInstituicao| Identificador da cooperativa |S||
|cpf| Cpf do usuário logado |S||
|status| Tipos de status de uma senha, caso não informado retornará senhas de todos os status |N| "aguardando", "atendendo", "atendida", "cancelada" |
|dataInicial| Data de início para busca de senhas | Requerido se não for informado o "idAtendimento" | data no formato "dd/mm/yyyy"|
|dataFinal| Data de termino para busca de senhas | Requerido se não for informado o "idAtendimento" |data no formato "dd/mm/yyyy"|
|idAtendimento| Identificador de uma senha | N | | 


**Exemplo de resposta**

```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDCooperativa": 4001,
      "SiglaInstituicao": "SICOOB EXECUTIVO",
      "IDUnidadeInst": 0,
      "NomeUnidade": "UNIDADE 0",
      "IDAtendimento": 175398,
      "SenhaFormatada": "PC0002",
      "DataEmissao": "14/08/2019 16:50:15",
      "IDStatus": 1,
      "DescStatus": "Aguardando",
      "IDDestino": 1,
      "DescDestino": "Caixa Teste",
      "TextoSenha": "Ei, vai no caixa ? Se utilizar o Sicoobnet, atm, ganhar� R$ 0,30 por cada boleto - convenio pago",
      "IDFila": 1,
      "NomeFila": "Preferencial",
      "IDCanalEmissao": 2,
      "DescCanal": "Aplicativo",
      "LinkServidorSenhas": "http://cpro29096.publiccloud.com.br:8085"
    },
  ]
}
```

---

## Cancela uma senha

> `[ DELETE ]`  O usuário poderá cancelar uma senha caso esteja como status "aguardando". Este endpoint será disponibilizado no servidor de cada cooperativa, de forma com que seu IP será usado na url em "linkCooperativa". Os dados de acessos serão os usuários e senhas de autenticação da Navega Consultoria em cada cooperativa.

```
{linkcooperativa}/navega/api/TEmissaoSenha/SenhaAplicativo?idInstituicao=343&idAtendimento=99999
```

**Exemplo de resposta**

```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDCooperativa": 4001,
      "SiglaInstituicao": "SICOOB EXECUTIVO",
      "IDUnidadeInst": 0,
      "NomeUnidade": "UNIDADE 0",
      "IDAtendimento": 175398,
      "SenhaFormatada": "PC0002",
      "DataEmissao": "14/08/2019 16:50:15",
      "IDStatus": 1,
      "DescStatus": "Aguardando",
      "IDDestino": 1,
      "DescDestino": "Caixa Teste",
      "TextoSenha": "Ei, vai no caixa ? Se utilizar o Sicoobnet, atm, ganhar� R$ 0,30 por cada boleto - convenio pago",
      "IDFila": 1,
      "NomeFila": "Preferencial",
      "IDCanalEmissao": 2,
      "DescCanal": "Aplicativo",
      "LinkServidorSenhas": "http://cpro29096.publiccloud.com.br:8085"
    },
  ]
}
```

---

## Informações adicionais

### Tipos de filas

|Id|Fila|Letra Senha|
|--|--|--|
|1|Preferencial| P | 
|2|Associados| A | 
|3|Não associados| N |
|4|Preferencial especial| E |

### Tipos de identificação
|Id|Tipo de identificação|
|--|--|
|0|Nenhum|
|1|Conta corrente|
|2|CPF / CNPJ| 
|3|Biometria| 
|4|Cód. Associado| 

