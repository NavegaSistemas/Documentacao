> `[ GET ]` Busca metas

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetasSituacao/{idSituacao}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idSituacao|Int|**Required** - Id da situação da meta|

---

## Detalhes de metas

> `[ GET ]` Busca os itens diários de uma meta em nível consolidado
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaConsolidado/{idMeta}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|

---

> `[ GET ]` Busca os itens diários de uma meta em nível de unidade

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaUnidade/{idMeta}/{idUnidade}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idUnidade|Int|**Required** - Id da unidade selecionada|

---

> `[ GET ]` Busca os itens diários de uma meta em nível de gerente
  
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaGerente/{idMeta}/{idGerente}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idGerente|Int|**Required** - Id do gerente selecionado|

---

> `[ GET ]` Busca os itens mensais de uma meta em nível consolidado
  
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalConsolidado/{idMeta}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|

---

> `[ GET ]`  Busca os itens mensais de uma meta em nível de unidade
  
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalUnidade/{idMeta}/{idUnidade}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idUnidade|Int|**Required** - Id da unidade selecionada|

---

> `[ GET ]` Busca os itens mensais de uma meta em nível de gerente

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalGerente/{idMeta}/{idGerente}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idGerente|Int|**Required** - Id do gerente selecionado|

---

## Itens de metas

> `[ GET ]` Busca a participação mensal de gerentes em um item de uma meta
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalItemGerentes/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|

---

> `[ GET ]` Busca a participação mensal de unidades em um item de uma meta

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalItemUnidades/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|

---

> `[ GET ]` Busca a participação mensal de regionais em um item de uma meta
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaMensalItemRegionais/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|

---

> `[ GET ]` Busca a participação diário de gerentes em um item de uma meta

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaItemGerentes/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|

---

> `[ GET ]` Busca a participação diário de unidades em um item de uma meta
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaItemUnidades/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|

---

> `[ GET ]` Busca a participação diário de regionais em um item de uma meta
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TMetas/MetaDiariaItemRegional/{idMeta}/{idItem}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idMeta|Int|**Required** - Id da meta|
|idItem|Int|**Required** - Id do item de uma meta|