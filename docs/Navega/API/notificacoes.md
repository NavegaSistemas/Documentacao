## Introdução

A Notificação é um método encontrado pela Navega Consultoria para se comunicar com os usuários de maneira fácil e simples, além de fornecer dados diários que são relevantes as Cooperativas. Rotinas da empresa gerão notificações que chegam ao usuário do Navega Mobile em formato de push notifications e ficam registradas dentro do aplicativo para eventuais consultas.


## Endpoints disponíveis

- [Busca notificações](#busca-notificacoes)
- [Apaga uma notificação](#apaga-uma-notificacao)
- [Notificação como lida](#notificacao-como-lida)

## Busca notificações
> `[ GET ]`  O método de buscar notificações é utilizado para obter as notificações direcionadas à um usuário logado. Estas notificações podem ser filtradas por intervalo de datas, status e paginação.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/notifications?&page={}&status={}&dataInicial={}&dataFinal={}
```

### Exemplo de reposta

```
{
  "pages": 26,
  "result": [
    {
      "IDLogin": "Navega4133_00",
      "IDNotificacao": "84C7A114-F048-4340-9A29-02F66D6A453F",
      "BolLida": false,
      "DataReferencia": "28/10/2019",
      "DataNotificacao": "28/10/2019",
      "Titulo": "Os associados listados abaixo ficarão inativos em breve",
      "Subtitulo": "",
      "BolPush": true,
      "IDPush": "559972f2-bb5f-4836-96c6-138c911430b8",
      "Texto": [
        "JOAO ALVES MOREIRA, "
      ]
    },
  ],
}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|page|Int|Paginação do endpoint|S|Números inteiros positivos|As páginas começam pelo número 1|
|status|String|Status das notificações|S|String **lidas**, **naolidas** ou **todas**||
|dataInicial|String|Data de início do intervalo de datas de notificações.|S|Datas no formato **DD/MM/YYYY**|
|dataFinal|String|Data de termino do intervalo de datas de notificações.|S|Datas no formato **DD/MM/YYYY**|

---

## Apaga uma notificação 
> `[ DELETE ]`  Marca uma notificação como apagada
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/notifications?&idnotificacao={}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idnotificacao|Int|Id da notificação que será apagada|S|Números inteiros positivos| Este ID é obtido através do [endpoint](#busca-notificacoes) que disponibiliza as notificações|

---

## Notificação como lida
> `[ POST ]` Muda o status de uma notificação para lida. Este método é utilizado quando o usuário abre uma notificação que estava com o status de não lida anteriormente.
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/lida?&idnotificacao={}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idnotificacao|Int|Id da notificação que será marcada como lida|S|Números inteiros positivos| Este ID é obtido através do [endpoint](#busca-notificacoes) que disponibiliza as notificações|
