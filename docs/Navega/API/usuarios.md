### Busca de usuários
> `[ GET ]`  Busca dados dos usuários do sistema
 
```
http://cpro29096.publiccloud.com.br:8080/navega/api/TAcessos/Usuarios/{idLogin}
```

**Exemplo de resposta**
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
      "NomeCompleto": "Jo�o da Silva",
      "NomeTratamento": "Jo�o",
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

**Dicionário de dados**

|Chave|Tipo|Descrição|Requerido|Observações|
|--|--|--|--|--|
|idLogin|Int|Identificador para login do usuário| N | Caso não seja informador irá retornar informações de todos os usuários cadastrados |

---