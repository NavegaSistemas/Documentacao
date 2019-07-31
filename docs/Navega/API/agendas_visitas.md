### > Check-in e Check-out

> `[ PUT ]`  Grava o check-in ou check-out de uma agenda de visitas.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TAgendaVisita/Check
```
Os parâmetros são passados no body da requisição no formato JSON.

|Chave|Tipo|Descrição|Requerido|Observações
|----|------|--------|--------|--------|
|idAgenda|Int| Código da agenda | S | |
|tipoCheck|String|Tipo do check| S | valores possíveis: *checkin* ou *checkout*
|latitude|Float| Latitude da localização no momento do check | S | |
|longitude|Float| Longitude da localização no momento do check | S | |

### Check-in e Check-out
> `[ PUT ]`  Grava o check-in ou check-out de uma agenda de visitas.
 
```
http://cpro29096.publiccloud.com.br:8080/navega/api/TAgendaVisita/Check
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idLogin|Int|Login do usuário|N|Caractéres|Caso não seja informado irá retornar todos os usuários da instituição do usuário logado|

---