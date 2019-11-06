## Introdução

As agendas gerenciais são utilizadas pelos gerentes das Cooperativas paara organizar as visitas aos seus associados. Cada gerente é responsável por um conjunto de associados e é normal que consultas sejam feitas para acompanhamento de algum projeto, ou outros tarefas. 

## Endpoint disponíveis

- [Busca gerentes com agendas](#busca-gerentes-com-agendas)
- [Busca todas as agendas de um gerente](#busca-agendas-de-um-gerente)
- [Fazer check-in e check-out](#check-in-e-check-out)
- [Cancela check-in](#cancela-check-in)
- [Cancela uma agenda](#cancela-uma-agenda)
- [Reagenda uma agenda](#reagenda-uma-agenda)
- [Encerra uma agenda](#encerra-uma-agenda)
- [Adiciona foto](#adiciona-foto)
- [Busca fotos de uma agenda](#busca-fotos)


## Busca gerentes com agendas

> `[ GET ]` Lista todos os gerentes que possuem alguma agenda gerencial relacionada à eles.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/GerentesAgendasAbertas
```

### Exemplo de resposta

```
{
  "Result": [
    {
      "IDInstituicao": 343,
      "IDGerente": 1260567,
      "NomeGerente": "ADRIANO SANTOS DA SILVA",
      "NomeTratamento": "ADRIANO SANTOS",
      "AgendasAbertas": 3
    },
  ]
}
```

---

## Busca agendas de um gerente

> `[ GET ]` Lista todas as agendas gerenciais de um gerente em específico. É importante mencionar que as agendas são categorizadas e separadas por data. As agendas que estão mais próximas são exibidas primeiro.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/AgendaVisitaData?gerente={idGerente}
```

### Exemplo de resposta

```
{
  "Result": [
    {
      "dataVisita": "2019-03-05T00:00:00.000-03:00",
      "agendas": [
        {
          "IDAgenda": 104,
          "IDOrigemAgenda": 1,
          "DescOrigemAgenda": "Manual",
          "IDOrigemPessoa": 1,
          "IDCliente": 1335995,
          "IDClienteSisbr": 277843,
          "NomeCliente": "ADENISIO PEREIRA DE LIMA",
          "IDMensagem": "",
          "BolReagendada": 1,
          "IDAgendaAnterior": 55,
          "IDUnidadeInst": 0,
          "NomeUnidade": "UNIDADE 0",
          "IDGerente": 1260567,
          "NomeGerente": "ADRIANO SANTOS DA SILVA",
          "DataAgendamento": "29/08/2018 12:02:29",
          "DataVisita": "05/03/2019",
          "DescObservacao": "Originada da agenda nº 55",
          "BolClienteLocalizado": 0,
          "IDSituacao": 1,
          "IDCheck": 2,
          "DescSituacao": "Agendada",
          "DescCheck": "Em Checkout",
          "DataUltimaSituacao": "04/03/2019 09:14:15",
          "Usuario": "mob4001_00",
          "NumTelefone": "(61) 996861202",
          "Objetivos": [
            {
              "IDObjetivo": 2,
              "DescObjetivo": "Capitalização",
              "DescObservacao": "",
              "BolExpectativa": false,
              "BolNovaVisita": false,
              "DataNovaVisita": ""
            }
          ]
        },
      ]
    },
  ]
}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idGerente|Int|Identificador do gerente|S|Número inteiros positivos|Corresponde ao **IDGerente** presente na [listagem de gerentes com agendas](#busca-gerentes-com-agendas)|

---

## Check-in e Check-out

> `[ PUT ]`  Grava o check-in ou check-out de uma agenda de visitas. Os parâmetros são enviados pelo body da requisição.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/Check
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |
|tipoCheck|String|Tipo do check| S | *"checkin"* <br> *"checkout"* (sem aspas)
|latitude|Float| Latitude da localização no momento do check | S | ||
|longitude|Float| Longitude da localização no momento do check | S | ||

---

## Cancela check-in

> `[DELETE]` Logo após realizar um check-in em uma agenda, é possui cancelar o mesmo caso alguma eventualidade tenha acontecido.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/Checkin/{idAgenda}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |

---

## Cancela uma agenda

> `[POST]` Cancela uma agenda caso seja necessário. Os parâmetros são enviados no body da requisição

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/AgendaVisita
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|IDAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |
|IDAcao|Int| Código que define qual ação está sendo feito sobre uma agenda gerencial | S | Números inteiros positivos | Veja a [tabela de ações](#tabela-de-acoes) disponível. Para este caso é usado o ID **2** |

---

## Reagenda uma agenda

> `[POST]` Cancela uma agenda caso seja necessário. Os parâmetros são enviados no body da requisição

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/AgendaVisita
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|IDAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |
|IDAcao|Int| Código que define qual ação está sendo feito sobre uma agenda gerencial | S | Números inteiros positivos | Veja a [tabela de ações](#tabela-de-acoes) disponível. Para este caso é usado o ID **4**  |
|DataVisita|String| Nova data para agenda | S | Data no formato **DD/MM/YYYY** | |

---

## Encerra uma agenda

> `[POST]` Quando uma visita é feita, a agenda relacionada a ele é encerrada e dados relacionados a visita são fornecidos por meio deste endpoint.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/AgendaVisita
```

### Exemplo de body da requisição

```
{
  IDAcao: 3,
  IDAgenda: 100,
  LocalizouCliente: true,
  Objetivos: [
    {
      IDObjetivo: 1,
      Observacao: "Observação de teste",
      GerouExpectativa: true,
      NovaVisita: true,
      DataNovaVisita: 30/12/2018
    },
  ]
}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|IDAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |
|IDAcao|Int| Código que define qual ação está sendo feito sobre uma agenda gerencial | S | Números inteiros positivos | Veja a [tabela de ações](#tabela-de-acoes) disponível. Para este caso é usado o ID **3** |
|LocalizouCliente|Boolean|Informação fornecida pelo gerente que informa se o associado foi encontrado ou não durante a visita|S|True, False| |
|Objetivos|Array de objetos| Um array que contêm informações de todos os objetivos da agenda gerencial|S|||

---

## Adiciona foto

> `[POST]` Cancela uma agenda caso seja necessário. Os parâmetros são enviados no body da requisição

```
https://upload-files-backend.herokuapp.com/schedule
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|IDAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |
|file|file| Foto a ser associada a agenda | S | Tipo file | |
|Descricao|String| Descrição da foto | S | | |

---

## Busca fotos

> `[GET]` Lista todas as fotos que foram relacionadas a uma determinada agenda gerencial

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAgendaVisita/Foto/{idAgenda}
```

### Exemplo de resposta

```
{
	"Result": [
    {
      "DataHoraRegistro": "22/03/2019 11:51:52",
      "Descricao": "Teste",
      "IDFoto": "64c543d0-4cb2-11e9-b44e-4733dc33782a",
      "Link": "https://firebasestorage.googleapis.com/v0/b/navega-470d8.appspot.com/o/debug%2F343%2FAgendas%2F104%2F64c543d0-4cb2-11e9-b44e-4733dc33782a.jpg?alt=media&token=7180e6ce-d4dc-4f24-b7cb-95a882f9676d"
    },
  ]	
}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idAgenda|Int| Código da agenda | S | Números inteiros positivos | Corresponde ao **IDAgenda** presente na [listagem de agendas](#busca-agendas-de-um-gerente) |

---

## Informações adicionais

### Tabela de ações

|id|ação|
|--|--|
|1|Agendamento|
|2|Cancelamento|
|3|Encerramento|
|4|Reagendamento|
|5|Check in|
|6|Check out|
|7|Check in cancelado|
