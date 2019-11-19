## Introdução

A *Navega Consultoria* possui um sistema de cadastrado de usuários que possuem permissões para acesso aos serviços da empresa. Este cadastrado é realizado através do Navega Desktop já no ambiente de produção nas cooperativas parceiras. Portanto todos os dados relacionados ao cadastro de usuários são armazenados localmente em cada instuição e periodicamente são enviados para o ambiente cloud da Navega, assim possibilitando a integração com o sistema mobile.

## Endpoints disponíveis

- [Busca de usuários](#busca-de-usuarios)
- [Preferências de usuário](#preferencias-de-usuario)

## Busca de usuários
> `[ GET ]`  Busca dados dos usuários do sistema, caso um id seja especificado irá retornar apenas um usuário, caso contrário, todos os usuários serão exibidos. A autenticação é feita através deste endpoint, caso este usuário não exista, irá ser retornado um array vazio dentro da chave "Usuarios", caso contrário as informações serão disponibilizadas e será permitido o acesso para este usuário.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TAcessos/Usuarios/{idLogin}
```

### Exemplo de resposta

```
{
  "Usuarios": [
    {
      "IDLogin": "mob4001_00",
      "IDInstituicao": 343,
      "IDUsuario": 5,
      "NumCooperativa": 4001,
      "IDUnidadeInst": 0,
      "NomeUnidade": "UNIDADE 0",
      "IDCliente": 1260567,
      "NumCpf": "",
      "Senha": "202CB962AC59075B964B07152D234B70",
      "NomeCompleto": "João da Silva",
      "NomeTratamento": "João",
      "IDGrupoFuncao": 1,
      "DescGrupoFuncao": "Presidente",
      "BolGerente": false,
      "BolAtivo": true,
      "BolAcessoMobile": false,
      "IDPerfil": 2,
      "BolExpira": false,
      "BolAcessoConsolidado": true,
      "BolAcessoUnidade": true,
      "BolAcessoGerente": true,
      "BolAcessoCliente": true,
      "IDSetorInstituicao": 0,
      "DescSetorInstituicao": "",
      "Email": "",
      "IDNivelSaldo": 1,
      "DescNivelSaldo": "Consolidado",
      "DescGrupo": "ADM"
    }
  ]
}
```

### Dicionário de dados

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idLogin|Int|Identificador para login do usuário| N | Caso não seja informador irá retornar informações de todos os usuários cadastrados |

---


## Preferências de usuário
> `[ GET ]`  Busca as preferências em relação ao tipo de saldo e periodicidade escolhidos pelo usuário para realizar consultas das contas gerenciais. Os id`s para tipos de saldos estão presentes na [tabela de tipos de saldo](#tipos-de-saldo). O Campo **IDDiaSemana** corresponde a [tabela de dias da semana](#dias-da-semana) e o **IDTipoPeriodicidade** a [tabela de periodicidades](#periodicidades)

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/PreferenciasConsultas
```

### Exemplo de resposta

```
{
  "IDTipoSaldoPatrimonial": 1,
  "IDTipoSaldoResultado": 4,
  "IDDiaSemana": 3,
  "IDTipoPeriodicidade": 3,
  "QtdPeriodos": 7
}
```

## Atualiza prefêrencias de usuário
> `[ GET ]`  Atualiza as informações de preferência de um usuário

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TContasGerenciais/PreferenciasConsultas
```

### Exemplo de body da requisição

```
{
  "IDTipoSaldoPatrimonial": 1,
  "IDTipoSaldoResultado": 4,
  "IDDiaSemana": 3,
  "IDTipoPeriodicidade": 3,
  "QtdPeriodos": 7
}
```

### Dicionário de dados

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|IDTipoSaldoPatrimonial|Int|Id do tipo de saldo para contas patrimoniais|S| 1 ou 2 | Corresponde aos tipos de saldos *Final* ou *Médio* presentes na [tabela de tipos de saldo](#tipos-de-saldo)|

## Informações adicionais

### Tipos de saldo

|ID|Descrição|Sigla|
|--|--|--|
|1|Final|FIN|
|2|Médio|MDU|
|3|Período|PER|
|4|Acumulado|ACU|
|5|Corporativo|COR|
|6|Índice|IND|
|7|Personalizado|PER|


### Dias da semana

|ID|Descrição|
|--|--|
|1|Domingo|
|2|Segunda-Feira|
|3|Terça-Feira|
|4|Quarta-Feira|
|5|Quinta-Feira|
|6|Sexta-Feira|
|7|Sábado|

### Periodicidades

|ID|Descrição|
|--|--|
|1|Diario|
|2|Semanal|
|3|Mensal|
