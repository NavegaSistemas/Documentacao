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
