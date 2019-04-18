> `[ GET ]` Busca todas as notificações do usuário logado
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/notifications?&page={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|page|Int|**Required** - Paginação do endpoint|

---

> `[ DELETE ]` Apaga uma notificação
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/notifications?&idnotificacao={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idnotificacao|Int|**Required** - Id da notificação que será apagada|

---

> `[ POST ]` Marca uma notificação como lida
 
```
http://cpro29096.publiccloud.com.br:8082/navega/api/TNotifications/lida?&idnotificacao={}
```

|Parâmetro|Tipo|Descrição
|----|------|--------|
|idnotificacao|Int|**Required** - Id da notificação que será marcada como lida|
