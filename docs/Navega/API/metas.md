## Cadastro de metas
> `[ GET ]` Busca metas

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetasSituacao/{idSituacao}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idSituacao|Int|**Required** - Id da situação da meta|

---

## Acompanhamento da realização das metas

---

### > MetaRealizada

> `[ GET ]` Consulta todos os itens de uma determinada meta em uma determinada data.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TMetas/MetaRealizada?nivelsaldo={nivelsaldo}&periodicidade={periodicidade}&idMeta={idMeta}&identificador={identificador}&dataReferencia={dd/mm/yyy}

```
|Parâmetro|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|nivelSaldo|String| nível do saldo da meta| S | Valores possíveis: *consolidado, unidade, gerente, regional*|
|periodicidade|String|periodicidade de acompanhamento da meta| S | Valores possíveis: *mensal, diaria*|
|idMeta|Int|id da meta| S | |
|identificador|Int| relacionado ao nível de saldo informado.| S* | Ex.: se o nível de saldo for *unidade*, o identificador é o código da unidade. **< Requerido se nível de saldo diferente de consolidado >**|
|dataReferencia|Date| data de referência da meta no formato *DD/MM/YYYY* | N | Caso seja mensal, o dia será sempre **01**. Se não informado será considerada a última data disponível.

---

### > MetaRealizadaHistorico

> `[ GET ]` Consulta o histórico de um item de uma meta.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TMetas/MetaRealizadaHistorico?nivelsaldo={nivelsaldo}&periodicidade={periodicidade}&idMeta={idMeta}&identificador={identificador}&idItem={idItem}

```
|Parâmetro|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|nivelSaldo|String| nível do saldo da meta| S | *Valores possíveis:* consolidado, unidade, gerente, regional|
|periodicidade|String|periodicidade de acompanhamento da meta| S | mensal, diaria|
|idMeta|Int|id da meta| S | |
|identificador|Int| relacionado ao nível de saldo informado.| S* | Ex.: se o nível de saldo for *unidade*, o identificador é o código da unidade. **< Requerido se nível de saldo diferente de consolidado >**|
|idItem|Int| id do item da meta | S |


---

### > MetaRealizadaItem

> `[ GET ]`  Consulta a realização de um item de uma meta para todas as unidades, gerentes ou regionais, em uma data específica.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TMetas/MetaRealizadaItem?nivelsaldo={nivelsaldo}&periodicidade={periodicidade}&idMeta={idMeta}&identificador={identificador}&idItem={idItem}&dataReferencia={dd/mm/yyy}

```
|Parâmetro|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|nivelSaldo|String| nível do saldo da meta| S | *Valores possíveis:* consolidado, unidade, gerente, regional|
|periodicidade|String|periodicidade de acompanhamento da meta| S | mensal, diaria|
|idMeta|Int|id da meta| S | |
|identificador|Int| relacionado ao nível de saldo informado.| S* | Ex.: se o nível de saldo for *unidade*, o identificador é o código da unidade. **< Requerido se nível de saldo diferente de consolidado >**|
|idItem|Int| id do item da meta | S |
|dataReferencia|Date| data de referência da meta no formato *DD/MM/YYYY* | N | Caso seja mensal, o dia será sempre **01**. Se não informado será considerada a última data disponível.
