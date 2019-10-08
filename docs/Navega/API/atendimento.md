## Acompanhamento de dados de atendimento

> `[ GET ]`  Busca um resumo do histórico de atendimento do dia em todas as unidades de uma cooperativa

```
http://cpro29096.publiccloud.com.br:8082/navega/api/TBiometriaAtendimento/EstatisticaResumo
```

**Exemplo de resposta**

```
{
  "DataEstatistica": "01/10/2019 16:27:59",
  "Consolidado": {
    "AtendimentosRealizados": 325,
    "PessoasNaFila": 0,
    "TempoMedioAtendimento": "00:09:02",
    "TempoMedioFila": "00:07:03"
  },
  "Unidades": [
    {
      "IDUnidadeInst": 0,
      "NomeUnidade": "SEDE PIRAPORA",
      "AtendimentosRealizados": 163,
      "PessoasNaFila": 0,
      "TempoMedioAtendimento": "00:07:51",
      "TempoMedioFila": "00:07:45"
    },
    {
      "IDUnidadeInst": 1,
      "NomeUnidade": "PA VARZEA DA PALMA",
      "AtendimentosRealizados": 94,
      "PessoasNaFila": 0,
      "TempoMedioAtendimento": "00:09:04",
      "TempoMedioFila": "00:04:51"
    },
  ]
}
```