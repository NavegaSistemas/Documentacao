#### Busca notificações
> `[ GET ]`  O método de buscar notificações é utilizado para obter as notificações direcionadas à um usuário logado. Estas notificações podem ser filtradas por intervalo de datas, status e paginação.

```
http://cpro29096.publiccloud.com.br:8080/navega/api/TNotifications/notifications?&page={}&status={}&dataInicial={}&dataFinal={}
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|page|Int|Paginação do endpoint|S|Números inteiros positivos|As páginas começam pelo número 1|
|status|String|Status das notificações|S|String **lidas** ou **naolidas**||
|dataInicial|String|Data de início do intervalo de datas de notificações.|S|Datas no formato **DD/MM/YYYY**|
|dataInicial|String|Data de termino do intervalo de datas de notificações.|S|Datas no formato **DD/MM/YYYY**|

---

#### Apaga uma notificação 
> `[ DELETE ]`  Marca uma notificação como apagada
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/notifications?&idnotificacao={}
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idnotificacao|Int|Id da notificação que será apagada|S|Números inteiros positivos||

---

#### Notificação como lida
> `[ POST ]` Muda o status de uma notificação para lida. Este método é utilizado quando o usuário abre uma notificação que estava com o status de não lida anteriormente.
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/lida?&idnotificacao={}
```

|Parâmetro|Tipo|Descrição|Requerido|Valores válidos|Observações|
|--|--|--|--|--|--|
|idnotificacao|Int|Id da notificação que será marcada como lida|S|Números inteiros positivos||
