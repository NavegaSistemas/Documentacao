## Introdução

Em termos gerais, o Product BackLog é uma listagem de todos os afazeres pendentes no projeto. Ele substitui o modelo tradicional de especificação de artefatos. Cada elemento da listagem é elicitado por meio de interação da equipe de desenvolvimento com o Cliente - podendo ser apenas um representante, o que torna os elementos levantados muito arbitrários; ou podendo ser uma equipe representante do Cliente, representando as diversas áreas que utilizarão o produto.

## Temas
|Tema|Descrição|Épicos|
|--|--|--|
|T1 - Informações|Envolve documentações, ajudas e sugestões dentro do app| > [Documentos](#ep01-documentos) <br> > [Suporte](#ep02-suporte) |
|T2 - Cadastro & Autenticação|Engloba toda a parte de cadastro, login, logout e chaves de acesso| > [Cadastro](#ep03-cadastro) <br> > [Login & Logout](#ep04-login-logout) <br> > [Código de segurança](#ep05-codigo-de-seguranca) |
|T3 - Controle gerencial|Engloba toda a parte de controle gerencial do aplicativo (o core da aplicação)| > [Acompanhamento de contas](#ep06-acompanhamento-de-contas) <br> > [Metas](#ep07-metas) <br> > [Painel Gerencial](#ep08-painel-gerencial) <br> > [Agenda](#ep09-agenda) <br> > [Fotos de Associados](#ep10-fotos-de-associados) |
|T4 - Configurações| Envolve toda a parte de prefêrencias e ajustes de um usuário ( ajustes do app ) | > [Perfil do usuário](#ep11-perfil-do-usuario) <br> > [Ajustes de consultas de contas](#ep12-ajustes-de-consultas-de-contas) <br> > [Temas](#ep13-temas)|
|T5 - Notícias | Envolve as informações de acompanhamento das cooperativas (Por exemplo, dados de atendimentos e de notícias) | > [Atendimento](#ep14-atendimento) <br> > [Noticias](#ep15-noticias) |
|T6 - Comunicação| Engloba a comunicação entre os usuários do app | > [Chat](#ep16-chat) |
|T7 - Testes| Envolve testes que garantem boa eficiência da aplicação | >[Testes](#ep17-testes)|

## Índices de US's
|Tema|Épico|ID & Nome|
|--|--|--|


## EP01 - Documentos 

#### US01 Disponibilizar política de privacidade & termos de uso

|US01|Disponibilizar politica de privacidade & termos de uso|
|--|--|
|**Versão**|Atual: 1.0 (07/06/2019) <br> Anterior: --|
|**Eu como**|Desenvolvedor|
|**Desejo**|Disponibilizar politica de privacidade & termos de uso|
|**Para que eu possa**|Informar o usuário sobre os termos do app|
|**Pontos**|5|
|**Prioridade**|Could|
|**Critérios de aceitação**| > Deve seguir o padrão deste tipo de documento <br> > Deve conter todos os termos necessários <br> > Deve ter uma politica de privacidade clara|

#### US02 Elaborar testes de usabilidade

| **US02** | **Elaborar testes de usabilidade**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Elaborar testes de usabilidade com os usuários |
| **Para que eu possa** | Para avaliar maiores dúvidas de usabilidade |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve disponibilizar Documentação; <br> > Deve mostrar dúvidas frequentes; <br> > Deve informar usuário de como funciona o aplicativo; <br> > Deve criar cenários e tarefas; <br> Deve usar alguma escala para medição da dificuldade de uma tarefa |

#### US03 Documentar e agrupar dúvidas dos usuários

| **US03** | **Documentar e agrupar dúvidas dos usuários**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Documentar e agrupar dúvidas dos usuários |
| **Para que eu possa** | Disponibilizar respostas de forma simples e objetiva |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve disponibilizar ao usuário dúvidas básicas; <br> > Aplicativo deve explicar quaisquer funcionalidade; <br> > Deve usar informações intuitivas; <br> > Deve atualizar com frequência as dúvidas conforme atualizações do aplicativo. |

#### US04 Medir eficiência da resposta para uma pergunta

| **US04** | **Medir eficiência da resposta para uma pergunta**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Medir eficiência da resposta para uma pergunta |
| **Para que eu possa** | Decidir se há necessidade de aprimoração de explicações sobre um item |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve estabelecer um tempo médio para as funcionalidades; <br> > Deve mostrar funcionalidades da melhor forma e rapidez; <br> > Deve tratar perdas de eficiência; <br> > Deve tratar dados que sejam necessários; <br> > Deve haver exceções para quantidade e qualidade. |

#### US05 Fornecer informações da Empresa

| **US05** | **Fornecer informações da Empresa**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Fornecer informações da Empresa |
| **Para que eu possa** | Informar ao usuário maiores detalhes sobre a Navega Consultoria e aumentar a confiança nos serviços |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar uma imagem clara e objetiva da empresa <br> > Deve utilizar informações que dêem confia para o usuário <br> > Deve mostrar os responsáveis pela empresa |

## EP02 - Suporte

#### US06 - Enviar sugestões de melhoria/feedback

| **US06** | **Enviar sugestões de melhoria/feedback**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Enviar sugestões de melhoria/feedback |
| **Para que eu possa** | Dar sugestões de como gostaria que o app fosse, para que futuramente sejam atendidas |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve enviar informações relevantes; <br> > Deve filtrar boas propostas de melhoria <br> Analisar possibilidade de mplementação; <br> > Enviar feedback para o usuário. |

## EP03 - Cadastro

#### US07 - Informar o fluxo de cadastro

| **US07** | **Informar o fluxo de cadastro**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Informar o fluxo de cadastro |
| **Para que eu possa** | Informar ao usuário como o cadastro é feito. |
| **Pontos** | 1 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve informar como o cadastro é feito; <br> > Deve justificar porque o cadastro não é feito pelo app; <br> > Deve possui informações claras e objetivas. |

## EP04 - Login & Logout

#### US08 - Validar informações de login

| **US08** | **Validar informações de login**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Validar informações de login |
| **Para que eu possa** | Realizar o login do usuário corretamente  |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve enviar um feedback caso aconteça algum erro; <br> > Deve enviar requisição de autenticação apenas quando existirem dados; |

#### US09 - Recuperar senha

| **US09** | **Recuperar senha**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Recuperar senha |
| **Para que eu possa** | Me logar na aplicação caso tenha esquecido minha senha |
| **Pontos** | 1 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve informar ao usuário como deve ser feita a recuperação de senha; <br> > Deve conter informações claras e objetivas  |

#### US10 - Persistir dados do usuário

| **US10** | **Persistir dados do usuário**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Persistir dados do usuário |
| **Para que eu possa** | Logar o usuário automaticamente caso ja tenha se logado anteriormente |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve persistir os dados do usuário em um banco local; <br> > Deve verificar se existem dados ao iniciar a aplicação <br> > Deve logar usuário automaticamente  |

#### US11 - Deletar dados do usuário

| **US11** | **Deletar dados do usuário**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Deletar dados do usuário |
| **Para que eu possa** | Deslogar usuário do app e de serviços externos (Firebase) |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve excluir os dados do usuário em um banco local; <br> > Deve deslogar de serviços externos (firebase) |

## EP05 - Acompanhamento de contas

#### US12 - Ver lista de contas

| **US12** | **Ver lista de contas**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Ver lista de contas  |
| **Para que eu possa** | Ver evolução de contas mais importantes de forma rápida |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve definir contas mais importantes; <br> > Deve buscar e mostrar contas <br> > Deve fornecer dados iniciais da evolução de contas |

#### US12 - Ver gráfico de uma conta

| **US12** | **Ver gráfico de uma conta**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Ver gráfico de uma conta |
| **Para que eu possa** | Acompanhar detalhadamente a evolução de uma conta |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve definir formato do gráfico; <br> > Deve definir cores representativas <br> > Deve mostrar dados de forma clara e objetiva <br> > Deve possuir evolução de valores em um certo periodo de tempo |

#### US13 - Ver dados de uma conta em nível consolidado e de unidades

| **US13** | **Ver dados de uma conta em nível consolidado e de unidades**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Ver dados de uma conta em nível consolidado e de unidades |
| **Para que eu possa** | Acompanhar evolução de uma conta em diferentes níveis de saldo |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar participação de todas as unidades dem relação a uma conta; <br> > Deve definir posição de cada unidade; <br> > Deve mostrar dados de forma clara e objetiva <br> > Deve possui evolução de valores em um certo periodo de tempo |

## EP06 - Metas

#### US14 - Visualizar metas e itens de metas

| **US14** | **Visualizar metas e itens de metas**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar metas e itens de metas |
| **Para que eu possa** | Acompanhar andamentos de metas ao passar do tempo |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar todas as metas da cooperativa; <br> > Deve conter percentual de conclusão de cada meta; <br> > Deve possuir cores representativas |

#### US15 - Filtrar visualização de metas

| **US15** | **Filtrar visualização de metas**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Filtrar visualização de metas |
| **Para que eu possa** | Visualizar dados de uma meta em relação a diferentes níveis de saldo  |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve filtrar por periodo; <br> > Deve filtrar por nível de saldo; <br> > Deve fornecer lista de unidades; <br> > Deve fornecer lista de gerentes. |

#### US15 - Sinalizar caso não existam metas

| **US15** | **Sinalizar caso não existam metas**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Sinalizar caso não existam metas |
| **Para que eu possa** | Fornecer um feedback visual para o usuário de quando não existirem metas cadastradas  |
| **Pontos** | 2 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve possuir uma imagem ilustrativa; <br> > Deve verificar se há metas. |

## EP07 - Painel gerencial

#### US15 - Sinalizar caso não existam metas

| **US15** | **Sinalizar caso não existam metas**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Sinalizar caso não existam metas |
| **Para que eu possa** | Fornecer um feedback visual para o usuário de quando não existirem metas cadastradas  |
| **Pontos** | 2 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve possuir uma imagem ilustrativa; <br> > Deve verificar se há metas. |

## EP08 - Agenda

## EP09 - Fotos de associados

## EP10 - Perfil do usuário

## EP11 - Ajustes de consultas de contas

## EP12 - Temas

## EP13 - Atendimento

## EP14 - Notícias

## EP15 - Chat




















