## Introdução

Uma nova funcionalidade do Navega Mobile é possibilitar com que os seus usuários gerentes das Cooperativas, neste caso, tenham a possibilidade de tirar fotos e registra-lás no aplicativo durante as visitas aos associados. As fotos serão organizadas em categorias e relacionadas aos associados. Cada associado possui um gerente responsável por ele.


## Busca associados com fotos
> `[ GET ]`  Listagem de todos os associados que já possuem alguma foto associada a eles.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/ClientesComFotos?page={page}&name={name}
```

**Exemplo de resposta**

```
{
  "pages": 1,
  "result": [
    {
      "IDCliente": 275903,
      "IDClienteSisbr": 197610,
      "NomeCliente": "SABINO PEREIRA FILHO",
      "NumCpfCnpj": "03678203663",
      "TipoPessoa": "PF",
      "IDGerente": 41008,
      "NomeGerente": "ODILON DE ARAUJO",
      "IDUnidadeInst": 0,
      "NomeUnidade": "SEDE PIRAPORA",
      "IDOrigemPessoa": 1,
      "DescOrigemPessoa": "Sisbr",
      "IDFoto": "6cd0757d74f0bc591619b4785d8e02c8-image-c9678214-785d-43ff-8499-7a2528929d7b.jpg",
      "LinkFoto": "https://navega-uploads.s3.amazonaws.com/6cd0757d74f0bc591619b4785d8e02c8-image-c9678214-785d-43ff-8499-7a2528929d7b.jpg",
      "DescFoto": "Teste",
      "DataHoraRegistro": "07/08/2019 14:46:45"
    }
  ]
}
```

**Dicionário de dados**

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|page|Int|Index para paginação do endpoint|S|Números inteiros positivos| A paginação deste endpoint possui início no index 1. A quantidade de páginas disponíveis se encontra na resposta deste endpoint na chave **pages**|
|name|String|Nome do associado|N| Nomes inteiros | Serão considerados trechos de nome que estão entre espaços. Por exemplo, caso o nome seja "Alan Lima", irá ter retorno das informações caso seja informado "Alan" ou "Lima". Uma string "Al" não será suficiente. |

---

## Busca fotos de um associado

> `[ GET ]` Busca dados sobre todas as fotos que foram relacionadas a algum associado. Um associado pode ter várias fotos associadas a ele, isto depende de quantas visitas o seu gerente responsável realizou, e também de quantas fotos foram tiradas.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/FotosCliente?idCliente={idCliente}&idCategoria={idCategoria}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idFoto": "6cd0757d74f0bc591619b4785d8e02c8-image-c9678214-785d-43ff-8499-7a2528929d7b.jpg",
      "idCategoria": 1,
      "categoria": "Teste",
      "idOrigemFoto": 1,
      "origemFoto": "Câmera",
      "linkFoto": "https://navega-uploads.s3.amazonaws.com/6cd0757d74f0bc591619b4785d8e02c8-image-c9678214-785d-43ff-8499-7a2528929d7b.jpg",
      "descFoto": "Teste",
      "dataHoraFoto": "07/08/2019 14:46:45",
      "idLogin": "Navega4133_00"
    },
  ]
}
```


**Dicionário de dados**

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idCliente|Int|Identificador do usuário em questão|S|Numérios inteiros positivos|Trata-se da chave **IDCliente** disponível na [listagem de associados com fotos](#busca-associados-com-fotos).|
|idCategoria|Int|Identificador da categoria onde estão as fotos|S|Numérios inteiros positivos|Trata-se da chave **IDCategoria** disponível na [listagem de categorias das fotos](#busca-categorias-de-fotos).|


---

## Adiciona uma nova foto

> `[ PUT ]` Adiciona uma foto e à associa a um associado e uma categoria de foto. Os parâmetros deste endpoint são enviados no body da requisição no formato JSON.

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

## Busca categorias de fotos

> `[ GET ]` Busca as categorias para fotos de associados, com possibilidade de filtrar por ativas e não ativas. Estas categorias são gerenciadas pelos usuários do Navega, sendo possível criá-las, edita-las e excluí-las.


```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto?status={}
```

**Exemplo de resposta**

```
{
  "Result": [
    {
      "IDCategoria": 1,
      "DescCategoria": "Teste",
      "CorCategoria": "#8B0000",
      "BolAtivo": true
    },
  ]
}
```

**Dicionário de dados**

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|status|String|Status das categorias|N|"**ativo**" (sem as aspas) <br> "**inativo**" (sem as aspas)|Caso nenhuma status seja informado, todas as categorias seram retornadas|

---

## Busca categorias de fotos de um associado

> `[ GET ]` Busca categorias relacionadas as fotos de um associado. Este endpoint é usada quando é necessário ter acesso a determinadas fotos de uma categoria de um associado.
  
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriasFotosCliente/{idCliente}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "id": 1,
      "descricao": "Teste",
      "cor": "#8B0000",
      "bolAtivo": true,
      "qtdFotos": 8
    },
  ]
}
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idCliente|Int|Identificador do usuário em questão|S|Numérios inteiros positivos|Trata-se da chave **IDCliente** disponível na [listagem de associados com fotos](#busca-associados-com-fotos).|

---

## Cria uma categoria

> `[ PUT ]` Cria uma nova categoria. Esta categoria poderá ser usada posteriormente para relacionar fotos de vários associados. Os parâmetros deste endpoint são enviados no body na requisição.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|id|Int|Identificador de categoria|S| Números inteiros positivos | Solicitado valor 0 para criação de uma nova categoria |
|nome|String|Nome da categoria|S| String de nome | |
|cor|String|Cor em hexadecimal que representa a categoria|S| Cores hexadecimais válidas | Uma "#" deve ser enviada, como por exemplo a cor '#F4AB80' |

---

## Edita uma categoria

> `[ POST ]` Edição de uma categoria pré existente

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|id|Int|Identificador da categoria a ser editada|S| Números inteiros positivos| Correspondente ao campo **IDCategoria** presente na [listagem de categorias](#busca-categorias-de-fotos) |
|nome|String| Nome da categoria| S | String de nome | | 
|cor|String|Cor em hexadecimal que representa a categoria|S| Cores hexadecimais válidas | Uma "#" deve ser enviada, como por exemplo a cor '#F4AB80' |

---

## Deleta uma categoria

> `[ DELETE ]` Inativação/Ativação de uma categoria

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/CategoriaFoto/{idCategoria}
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idCategoria|Int|Identificador da categoria|S| Números inteiros positivos| Correspondente ao campo **IDCategoria** presente na [listagem de categorias](#busca-categorias-de-fotos) |