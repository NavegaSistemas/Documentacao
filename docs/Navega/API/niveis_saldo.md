## Introdução

Os Níveis de Saldo são parâmetros utilizados para diversas consultas dentro do sistema da Navega Consultoria. 

* Uma Cooperativa de crédito possui **UNIDADES**, que são os seus pontos de atendimento, que podem ser vários dependendo de sua magnitude. 

* Possui **GERENTES** que são pessoas responsáveis pela gerência de cada unidade, de modo que uma unidade pode ter um ou vários gerentes e um gerente pode ser relacionado a uma ou várias unidades.

* E possui **REGIONAIS**, que são unidades de atendimento agrupadas a uma determinada região.

Todos estes níveis de saldo possuem indicativos para contas relacionadas a participação de cada um, além de várias outras tarefas dentro do sistema. Em vários ambientes dentro das aplicações da Navega estes níveis de saldo são unidos afim de criar um nível *CONSOLIDADO* para uma consulta mais geral por parte dos usuários.

## Busca unidades 

> `[ GET ]` Busca todas as unidades de uma cooperativa. Como não é informado nenhum parâmetro, as unidades que serão disponibilizadas estão associadas a mesma cooperativa do usuário logado no momento.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/Unidades
```

**Exemplo de resposta**

```
{
  "Unidades": [
    {
      "Codigo": 0,
      "Nome": "UNIDADE 0"
    },
  ]
}
```

---

## Busca gerentes

> `[ GET ]` Busca todas os gerentes de uma cooperativa. Como não é informado nenhum parâmetro, os gerentes que serão disponibilizados estão associados a mesma cooperativa do usuário logado no momento.

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TClientes/Gerentes
```

**Exemplo de resposta**
```
{
  "Gerentes": [
    {
      "Codigo": 1260567,
      "Nome": "ADRIANO SANTOS DA SILVA",
      "Tratamento": "ADRIANO SANTOS",
      "Ativo": true,
      "Unidade": "UNIDADE 0"
    },
  ]
}
```

---

## Busca regionais

> `[ GET ]` Busca todos os regionais de uma cooperativa. Como não é informado nenhum parâmetro, os regionais que serão disponibilizados estão associados a mesma cooperativa do usuário logado no momento. 

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TCorporativo/Regional
```

**Exemplo de reposta**

```
{
  "Result": [
    {
      "Codigo": 1,
      "Nome": "Regional 1 teste"
    },
  ]
}
```