As **variáveis de ambiente (Environment Variables)** são utilizadas para configurar o comportamento da aplicação sem a necessidade de alterar o código fonte. Esse padrão permite que a mesma aplicação seja executada em diferentes ambientes (desenvolvimento, homologação ou produção) apenas alterando valores de configuração.

No sistema **Navega**, as variáveis de ambiente são utilizadas principalmente para:

- Configuração de **portas de serviços**
- Definição de **URLs de APIs**
- Configuração de **conexão com banco de dados**
- Definição de **chaves de segurança**
- Identificação do **ambiente de execução**

Essas variáveis podem ser definidas diretamente no sistema operacional do servidor ou através de arquivos `.env`.

---

# Padrão de Nomenclatura

As variáveis seguem o padrão:

```
NVG_<CONTEXTO>_<CONFIGURAÇÃO>
```

Onde:

- **NVG** → Prefixo que identifica variáveis relacionadas ao sistema Navega
- **CONTEXTO** → Serviço ou componente da aplicação
- **CONFIGURAÇÃO** → Tipo de configuração da variável

Exemplos:

- `NVG_API_NAVEGA_NODEJS_PORT`
- `NVG_MYSQL_HOST`
- `NVG_INTERNAL_SERVICES_KEY`

Esse padrão facilita:

- Organização das variáveis
- Evitar conflitos com variáveis do sistema operacional
- Identificação rápida da finalidade de cada configuração

---

# Lista de Variáveis de Ambiente

| Variável                           | Descrição                                                                                                                    | Valor Default                                        |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| NVG_AGENT_DEPLOYMENT_NODEJS_PORT   | Porta do serviço **agent-deployment-nodejs**                                                                                 | `8000`                                               |
| NVG_API_NAVEGA_NODEJS_PORT         | Porta do serviço **api-navega-nodejs**                                                                                       | `8001`                                               |
| NVG_WEB_NAVEGA_RJS_PORT            | Porta do serviço **web-navega-rjs**                                                                                          | `8002`                                               |
| NVG_API_BACKOFFICE_NODEJS_BASE_URL | Base URL da API **Backoffice** no servidor Navega                                                                            | `http://navegasrvapp.eastus.cloudapp.azure.com:8085` |
| NVG_API_NAVEGA_NODEJS_BASE_URL     | Base URL da **API Navega** no servidor Navega                                                                                | `http://navegasrvapp.eastus.cloudapp.azure.com:8086` |
| NVG_MYSQL_HOST                     | Host do banco de dados **MySQL**                                                                                             | `127.0.0.1`                                          |
| NVG_MYSQL_DATABASE                 | Nome do banco de dados **MySQL**                                                                                             | `nvg`                                                |
| NVG_MYSQL_USER                     | Usuário de acesso ao banco **MySQL**                                                                                         | `Navega`                                             |
| NVG_MYSQL_PORT                     | Porta do banco de dados **MySQL**                                                                                            | `3308`                                               |
| NVG_MYSQL_PASSWORD                 | Senha de acesso ao banco **MySQL**                                                                                           | _(não definido)_                                     |
| NVG_IP_SERVER                      | IP do servidor da cooperativa onde os serviços estão sendo executados                                                        | _(não definido)_                                     |
| NVG_JWT_SECRET                     | Secret utilizado para geração e validação de tokens **JWT**                                                                  | _(não definido)_                                     |
| NVG_INTERNAL_SERVICES_KEY          | Chave de segurança utilizada para comunicação interna entre serviços. Funciona como um token de autenticação entre serviços. | `UUID()`                                             |
| NODE_ENV                           | Define o ambiente de execução da aplicação                                                                                   | `production`                                         |

---

# Exemplo de Configuração (.env)

```env
NVG_AGENT_DEPLOYMENT_NODEJS_PORT=8000
NVG_API_NAVEGA_NODEJS_PORT=8001
NVG_WEB_NAVEGA_RJS_PORT=8002

NVG_API_BACKOFFICE_NODEJS_BASE_URL=http://navegasrvapp.eastus.cloudapp.azure.com:8085
NVG_API_NAVEGA_NODEJS_BASE_URL=http://navegasrvapp.eastus.cloudapp.azure.com:8086

NVG_MYSQL_HOST=127.0.0.1
NVG_MYSQL_DATABASE=nvg
NVG_MYSQL_USER=Navega
NVG_MYSQL_PORT=3306
NVG_MYSQL_PASSWORD=

NVG_IP_SERVER=
NVG_JWT_SECRET=

NVG_INTERNAL_SERVICES_KEY=
NODE_ENV=production
```
