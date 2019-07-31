## Acompanhamento de contas

> `[ GET ]`  Busca acompanhamento de contas em nivel consolidado

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheAgoraConsolidado
```
 ---

> `[ GET ]` Busca acompanhamento de contas em nivel de unidade

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheAgoraUnidade/{idUnidade}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idUnidade|Int|**Required** - Id da unidade a ser consultada|

---

> `[ GET ]` Busca acompanhamento de contas em nivel de gerente

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheAgoraGerente/{idGerente}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idGerente|Int|**Required** - Id do gerente a ser consultado|

---

> `[ GET ]` Busca os detalhes de uma conta em relação a todas as unidades

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheAgoraContaUnidades/{idConta}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idConta|Int|**Required** - Id reduzido da conta a ser consultada|

---

> `[ GET ]` Busca os detalhes de uma conta em relação a todos os gerentes

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/AcompanheAgoraContaGerentes/{idConta}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idConta|Int|**Required** - Id reduzido da conta a ser consultada|


### > Acompanhe

> `[ GET ]`  Consulta a lista de todas as contas de acompanhamento da cooperativa ( consolidada ou de uma unidade ou de um gerente ).

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TContasGerenciais/Acompanhe?nivelSaldo={nivelSaldo}&identificador={identificador}
```
|Parâmetro|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|nivelSaldo|String| nível do saldo do acompanhamento | S | *Valores possíveis:* consolidado, unidade, gerente|
|identificador|Int| relacionado ao nível de saldo informado.| S* | Ex.: se o nível de saldo for *unidade*, o identificador é o código da unidade. **< Requerido se nível de saldo diferente de consolidado >**|



### > AcompanheItem

> `[ GET ]`  Consulta as unidades classificadas em ranking de um determinado item de acompanhamento.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TContasGerenciais/AcompanheItem?idAcompanhe{idAcompanhe}
```
|Parâmetro|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|idAcompanhe|Int| Código do tipo de acompanhamento | S | |
