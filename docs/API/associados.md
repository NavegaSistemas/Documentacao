## Busca de associados

> `[ GET ]` Busca todos os associados filtrando por nome ou cpf


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/ClientesResumido/{nome_cpf}/true
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|nome_cpf|String|**Required** - Substituir pelo nome ou cpf do associado|

---
 
## Fotos de associados

> `[ GET ]` Busca associados que ja possuem fotos associadas


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/ClientesComFotos?page={}&name={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|page|Int|**Not required** - Paginação do endpoint|
|name|String|**Not required** - Nome de uma pessoa para filtro de pesquisas|

---

> `[ GET ]` Busca fotos de um cliente


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/FotosCliente?idCliente={}&idCategoria={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idCliente|Int|**Required** - Id do cliente|
|idCategoria|Int|**Required** - Id da categoria|

---

> `[ PUT ]` Adiciona uma foto


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/FotoCliente
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idFoto|String|**Required** - Id da foto|
|idCliente|Int|**Required** - Id do associado que foi relecionado a uma foto|
|idOrigemPessoa|Int|**Required** - Id que representa a origem do cadastro de um associado. Caso seja 1 sua origem é do SisBr e 2 do Navega Sistemas|
|idCategoria|Int|**Required** - Id da categoria que foi relecionada a foto|
|link|String|**Required** - Link da foto após realizado seu upload em algum banco de dados|
|descricao|String|**Required** - Descrição de um foto|
|idOrigemFoto|Int|**Required** - Id relacionado a origem da foto. Usar 1 para câmera e 2 para galeria de fotos|

--- 

### Categorias de fotos

> `[ GET ]` Busca as categorias para fotos de associados, com possibilidade de filtrar por ativas e não ativas
  

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto?status={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|status|String|**Not required** - Valores possíveis: 'ativo', 'inativo'. Caso o parâmetro não seja passado, todas as categorias serão retornadas|

---

> `[ GET ]` Busca categorias relacionadas as fotos de um associado
  

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriasFotosCliente/{idCliente}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idCliente|Int|**Required** - Id do associado|

---

> `[ PUT ]` Cria uma nova categoria

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|id|Int|**Required** - Solicitado valor 0 para criação de uma nova categoria|
|nome|String|**Required** - Nome da categoria|
|cor|String|**Required** - Cor em hexadecimal que representa a categoria, por exemplo '#F4AB80'|

---

> `[ POST ]` Edição de uma categoria

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|id|Int|**Required** - Id da categoria editada|
|nome|String|**Required** - Nome da categoria|
|cor|String|**Required** - Cor em hexadecimal que representa a categoria, por exemplo '#F4AB80'|

---

> `[ DELETE ]` Inativação/Ativação de uma categoria

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto/{idCategoria}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idCategoria|Int|**Required** - Substituir pelo id da categoria|