## Busca unidades

> `[ GET ]` Busca dados de todos os pontos de atendimento disponíveis em um determinado raio de distância da localização do usuário. O raio de busca determinado foi de 100km.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TUnidades/UnidadesProximasRaio?latitude={latitude}&longitude={longitude}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idInstituicao": 343,
      "idCooperativa": 4001,
      "siglaInstituicao": "SICOOB EXECUTIVO",
      "idUnidadeInst": 0,
      "nomeUnidade": "UNIDADE 0",
      "descEndereco": "RUA LOCAL TESTE",
      "latitude": -15.836719,
      "longitude": -48.017172,
      "distancia": 0.587188801155316,
      "usuarioAssociado": false,
      "Horarios": [
        {
          "diaSemana": "Seg",
          "label": "Segunda-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "16:00:00"
        },
        {
          "diaSemana": "Ter",
          "label": "Terça-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Qua",
          "label": "Quarta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Qui",
          "label": "Quinta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Sex",
          "label": "Sexta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        }
      ],
      "Fotos": [
        {
          "idImagem": "4d40833d0d6655726bd7176b2144a7fc-aniversario,jpg.jpg",
          "linkImagemMaior": "https://navega-uploads.s3.amazonaws.com/4d40833d0d6655726bd7176b2144a7fc-aniversario%2Cjpg.jpg",
          "linkImagemMenor": ""
        }
      ]
    },
  ]
}
```


---

## Busca dados de uma unidade

> `[ GET ]` Busca dados específicos de uma unidade de atendimento, inclusive dados relativos aos destinos e filas de atendimentos disponíveis naquele local.

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TUnidades/UnidadeDetalhe?idInstituicao={idInstituicao}&idUnidadeInst={idUnidadeInst}
```

**Exemplo de resposta**
```
{
  "result": [
    {
      "idInstituicao": 475,
      "idCooperativa": 4133,
      "siglaInstituicao": "SICOOB SERTÃO",
      "linkServidorSenhas": "http://192.168.15.9:8080",
      "idUnidadeInst": 0,
      "nomeUnidade": "SEDE PIRAPORA",
      "idadeEspecial": 0,
      "descEndereco": "RUA ANTONIO NASCIMENTO",
      "descNumEndereco": "179",
      "descComplementoEndereco": "",
      "nomeBairro": "CENTRO",
      "nomeCidade": "PIRAPORA",
      "siglaUF": "MG",
      "numCEP": "39270000",
      "numTelefone": "",
      "latitude": -15.833448,
      "longitude": -47.955211,
      "usuarioAssociado": false,
      "horarios": [
        {
          "diaSemana": "Seg",
          "label": "Segunda-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "16:00:00"
        },
        {
          "diaSemana": "Ter",
          "label": "Terça-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Qua",
          "label": "Quarta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Qui",
          "label": "Quinta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        },
        {
          "diaSemana": "Sex",
          "label": "Sexta-feira",
          "horaInicial": "10:00:00",
          "horaFinal": "15:00:00"
        }
      ],
      "fotos": [
        {
          "idImagem": "128e2cc6bf5bc6c6ad20fa66e665a44d-imagem1.jpg",
          "linkImagemMaior": "https://navega-uploads.s3.amazonaws.com/128e2cc6bf5bc6c6ad20fa66e665a44d-imagem1.jpg",
          "linkImagemMenor": ""
        }
      ],
      "destinos": [
        {
          "idDestino": 1,
          "descricao": "Caixa",
          "letraSenha": "C",
          "textoSenha": "Vai no caixa? Evite ficar na fila e ainda ganhe R$ 0,31 por boleto pago no aplicativo Sicoobnet."
        },
        {
          "idDestino": 2,
          "descricao": "Atendimento",
          "letraSenha": "A",
          "textoSenha": "Já pensou em se aposentar com tranquilidade?\r\n Faça o Sicoob Previ\r\nMaiores informações no atendimento\r\n"
        },
        {
          "idDestino": 3,
          "descricao": "Consignados",
          "letraSenha": "E",
          "textoSenha": "Você esta fazendo uma excelente escolha, no Sicoob Sertão Minas você encontra as melhores taxas do mercado."
        },
        {
          "idDestino": 4,
          "descricao": "Gerência",
          "letraSenha": "G",
          "textoSenha": ""
        }
      ],
      "parametros": [
        {
          "idParametro": 36,
          "descricao": "Calcula atendimento preferencial automaticamente para Associados com base na idade ?",
          "valor": true
        }
      ]
    }
  ]
}
```


---

## Dados de localização

> `[GET]` Consulta os dados de localização de uma unidade

```
http://cpro29096.publiccloud.com.br:8084/navega/api/TUnidades/UnidadeLocalizacao?idInstituicao={idInstituicao}&idUnidadeInst={idUnidadeInst}
```

**Exemplo de resposta**

```
{
  "result": [
    {
      "idInstituicao": 475,
      "siglaInstituicao": "SICOOB SERTÃO",
      "idUnidadeInst": 0,
      "nomeUnidade": "SEDE PIRAPORA",
      "latitude": -15.833448,
      "longitude": -47.955211
    }
  ]
}
```

---

