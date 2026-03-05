As **variáveis de ambiente (Environment Variables)** são utilizadas para configurar o comportamento da aplicação sem a necessidade de alterar o código fonte. Esse padrão permite que a mesma aplicação seja executada em diferentes ambientes (desenvolvimento, homologação ou produção) apenas alterando valores de configuração.

No ecossistema do **Navega**, as variáveis de ambiente são utilizadas principalmente para:

- Configuração de **portas dos serviços**
- Definição de **endereços de APIs**
- Configuração de **conexão com banco de dados**
- Definição de **chaves de segurança**
- Definição do **ambiente de execução**

Essas variáveis geralmente são configuradas diretamente no servidor da cooperativa ou através de arquivos `.env`.

---

# Padrão de Nomenclatura

As variáveis seguem o padrão:

```
NVG_<CONTEXTO>_<CONFIGURAÇÃO>
```

Onde:

- **NVG** → Prefixo que identifica variáveis relacionadas ao sistema **Navega**
- **CONTEXTO** → Serviço ou componente da aplicação
- **CONFIGURAÇÃO** → Tipo de configuração da variável

Esse padrão traz algumas vantagens:

- Evita conflitos com variáveis do sistema operacional
- Facilita a identificação de configurações relacionadas ao Navega
- Padroniza o gerenciamento das variáveis entre os diferentes serviços

Exemplo:

```
NVG_API_NAVEGA_NODEJS_PORT
NVG_MYSQL_HOST
NVG_INTERNAL_SERVICES_KEY
```

---

# Lista de Variáveis de Ambiente

| Variável                             | Descrição                                                                                                                   | Valor Default                                        | Serviços que utilizam                                         |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------- |
| NVG_AGENT_DEPLOYMENT_NODEJS_PORT     | Porta do serviço **agent-deployment-nodejs**                                                                                | `8000`                                               | agent-deployment-nodejs                                       |
| NVG_API_NAVEGA_NODEJS_PORT           | Porta do serviço **api-navega-nodejs**                                                                                      | `8001`                                               | api-navega-nodejs                                             |
| NVG_WEB_NAVEGA_RJS_PORT              | Porta da aplicação web **Navega**                                                                                           | `8002`                                               | web-navega-nodejs                                             |
| NVG_API_BACKOFFICE_NODEJS_BASE_URL   | Base URL da **API Backoffice** no servidor Navega (cloud)                                                                   | `http://navegasrvapp.eastus.cloudapp.azure.com:8085` | api-navega-nodejs, web-navega-nodejs, agent-deployment-nodejs |
| NVG_API_NAVEGA_NODEJS_BASE_URL_LOCAL | Base URL da **API Navega** no servidor local da cooperativa                                                                 | _(não definido)_                                     | web-navega-nodejs                                             |
| NVG_MYSQL_HOST                       | Host do banco de dados **MySQL**                                                                                            | `127.0.0.1`                                          | api-navega-nodejs                                             |
| NVG_MYSQL_DATABASE                   | Nome do banco de dados **MySQL**                                                                                            | `nvg`                                                | api-navega-nodejs                                             |
| NVG_MYSQL_USER                       | Usuário de acesso ao banco **MySQL**                                                                                        | `Navega`                                             | api-navega-nodejs                                             |
| NVG_MYSQL_PORT                       | Porta do banco de dados **MySQL**                                                                                           | `3308`                                               | api-navega-nodejs                                             |
| NVG_MYSQL_PASSWORD                   | Senha do banco de dados **MySQL**                                                                                           | _(não definido)_                                     | api-navega-nodejs                                             |
| NVG_JWT_SECRET                       | Chave secreta utilizada para geração e validação de tokens **JWT**                                                          | _(não definido)_                                     | api-navega-nodejs                                             |
| NVG_INTERNAL_SERVICES_KEY            | Chave de segurança utilizada para comunicação interna entre serviços. Funciona como um token de autenticação entre serviços | `UUID()`                                             | api-navega-nodejs, agent-deployment-nodejs, web-navega-nodejs |
| NODE_ENV                             | Define o ambiente de execução da aplicação                                                                                  | `production`                                         | Todos os serviços                                             |

---

# Exemplo de Configuração (.env)

```env
NVG_AGENT_DEPLOYMENT_NODEJS_PORT=8000
NVG_API_NAVEGA_NODEJS_PORT=8001
NVG_WEB_NAVEGA_RJS_PORT=8002

NVG_API_BACKOFFICE_NODEJS_BASE_URL=http://navegasrvapp.eastus.cloudapp.azure.com:8085
NVG_API_NAVEGA_NODEJS_BASE_URL_LOCAL=

NVG_MYSQL_HOST=127.0.0.1
NVG_MYSQL_DATABASE=nvg
NVG_MYSQL_USER=Navega
NVG_MYSQL_PORT=3308
NVG_MYSQL_PASSWORD=

NVG_JWT_SECRET=
NVG_INTERNAL_SERVICES_KEY=

NODE_ENV=production
```
