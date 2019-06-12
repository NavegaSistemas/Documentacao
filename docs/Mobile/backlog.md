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
| **Prioridade** | Could |
| **Critérios de aceitação** | > Deve disponibilizar Documentação; <br> > Deve mostrar dúvidas frequentes; <br> > Deve informar usuário de como funciona o aplicativo; <br> > Deve criar cenários e tarefas; <br> > Deve usar alguma escala para medição da dificuldade de uma tarefa |

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
| **Critérios de aceitação** | > Deve enviar informações relevantes; <br> > Deve filtrar boas propostas de melhoria <br> > Analisar possibilidade de mplementação; <br> > Enviar feedback para o usuário. |

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

## EP07 - Painel gerencial

#### US16 - Visualizar contas gerenciais

| **US16** | **Visualizar contas gerenciais**|
|--|--|
| **Versão**| Atual: 1.0 (07/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar contas gerenciais |
| **Para que eu possa** | Fornecer principais contas de acompanhamento  |
| **Pontos** | 2 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar contas básicas |

#### US17 - Adicionar contas manualmente

| **US17** | **Adicionar contas manualmente**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Adicionar contas manualmente |
| **Para que eu possa** | Definir contas de meu interesse para visualização  |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar contas gerenciais <br> > Deve filtrar lista de contas <br> > Deve persistir contas adicionadas <br> > Deve possuir pesquisa por nome |

#### US18 - Mostrar gráficos de uma conta

| **US18** | **Mostrar gráficos de uma conta**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Mostrar graficos de uma conta |
| **Para que eu possa** | Informar os dados relacionados a uma conta em nível consolidado e gerentes de maneira fácil e simples |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve contar gráfico para uma conta em nivel consolidado <br> > Deve mostrar participação de unidades e gerentes <br> > Deve possuir cores |

#### US19 - Deletar contas manualmente

| **US19** | **Deletar contas manualmente**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Deletar contas manualmente |
| **Para que eu possa** | Ter controle de quais contas gostaria que fossem padrão  |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve apagar uma conta da lista do painel gerencial <br> Deve persistir os dados de contas em um banco local <br> Pedir confirmação de deleção  |

## EP08 - Agenda

#### US20 - Definir permissões de acesso de agendas

| **US20** | **Definir permissões de acesso de agendas**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Definir permissões de acesso de agendas |
| **Para que eu possa** | Apenas usuários com permissão acessem as agendas gerenciais  |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve retornar feedback para o usuário <br> > Deve mostrar agendas de acordo com a função do usuário |

#### US21 - Visualizar e editar agendas

| **US21** | **Visualizar e editar agendas**|
|--|--|
| **Versão**| Atual: 1.0 (12/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar e editar agendas |
| **Para que eu possa** | Interagir com as agendas gerenciais  |
| **Pontos** | 10 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar as agendas de um gerente <br> > Deve mostrar detalhes de uma agenda <br> > Deve cancelar agenda <br> > Deve reagendar uma agenda <br> > Deve encerrar uma agenda <br> > Deve fazer check-in e checkout <br> > Deve cancelar check-in <br> > Deve ligar para o associado |

#### US22 - Criar novas agendas gerenciais

| **US22** | **Criar novas agendas gerenciais**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Criar novas agendas gerenciais |
| **Para que eu possa** | Criar agendas de forma simples e fácil |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve criar agenda com descrição <br> > Deve criar agenda de forma simples e fácil |

## EP09 - Fotos de associados

#### US23 - Visualizar fotos de associados

| **US23** | **Visualizar fotos de associados**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar fotos de associados|
| **Para que eu possa** | Acompanhar e organizar fotos de associados |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve separar fotos por categorias <br> > Deve mostrar um feed de fotos para cada usuário <br> > Deve mostrar descrição de cada foto <br> > Deve possuir data de cada foto <br> > Deve sinalizar se a foto foi tirada da camêra ou da galeria |

#### US24 - Adicionar fotos de associados

| **US24** | **Adicionar fotos de associados**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Adicionar fotos de associados |
| **Para que eu possa** | Adicionar fotos para acompanhamento de associados  |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve possibilitar buscar fotos da galeria ou camêra <br> > Deve solicitar descrição da foto <br> > Deve relacionar cada foto a um associado <br> > Deve separar por categorias <br> > Deve criar novas categorias <br> Deve apagar categorias |

#### US25 - Apagar fotos de associados

| **US25** | **Apagar fotos de associados**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Apagar fotos de associados |
| **Para que eu possa** | Apagar uma foto caso seja enviada errôneamente |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve pedir confirmação do usuário <br> > Deve fornecer feedback sinalizando exclusão da foto |

#### US26 - Visualizar associados que possuem fotos

| **US26** | **Visualizar associados que possuem fotos**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar associados que possuem fotos|
| **Para que eu possa** | Acessar diretamente fotos de um associado em especifico |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve filtrar usuários <br> > Deve indicar dados do asssociado e do gerente |

## EP10 - Perfil do usuário

#### US27 - Editar foto de perfil

| **US27** | **Editar foto de perfil**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Editar foto de perfil |
| **Para que eu possa** | Adicionar novas fotos de perfil |
| **Pontos** | 3 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve permitir usar foto da câmeta ou galeria <br> > Deve cortar foto em um quadrado <br> Deve persistir apenas uma foto de perfil por usuário |

## EP11 - Ajustes de consultas de contas

#### US28 - Configurar periodos de saldos e tipos de contas

| **US28** | **Configurar periodos de saldos e tipos de contas**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Configurar periodos de saldos e tipos de contas |
| **Para que eu possa** | Controlar tipos de preferencias para consultas de contas gerenciais |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve configurar contas de usos e fontes <br> > Deve configurar contas de receitas e despesas <br> Deve configurar períodos de saldos de consulta |

## EP12 - Temas

#### US29 - Criar diferentes temas

| **US29** | **Criar diferentes temas**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Desenvolvedor |
|**Desejo** | Criar diferentes temas |
| **Para que eu possa** | Disponibilizar temas que agradem diferentes perfis de usuários |
| **Pontos** | 10 |
| **Prioridade** | Could |
| **Critérios de aceitação** | > Deve disponibilizar temas claros e escuros <br> > Deve persistir último tema escolhido <br> > Deve criar esquema de cores <br> Deve criar corpo do tema |

## EP13 - Atendimento

#### US30 - Visualizar dados de atendimento

| **US30** | **Visualizar dados de atendimento**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar dados de atendimento |
| **Para que eu possa** | Visualizar dados de atendimento de forma consolidada e por unidades |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar quantidade de pessoas na fila <br> > Deve mostrar quantidade de atendimentos já realizados <br> > Deve mostrar temp médio de atendimento <br> Deve mostrar tempo médio de espera na fila <br> > Deve atualizar informações automaticamente de x em x min |

## EP14 - Notícias

#### US31 - Visualizar notícias

| **US31** | **Visualizar notícias**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar notícias |
| **Para que eu possa** | Acessar as noticiais da minha cooperativa |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve filtrar notícias por não lidas <br> > Deve filtrar notícias por lidas <br> Deve filtrar notícias por todas <br> Deve filtrar notícias por período <br> Deve ilustrar notícias |

#### US32 - Apagar notícias

| **US32** | **Apagar notícias**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Apagar notícias |
| **Para que eu possa** | Apagar notícias que não desejo mais ver |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve pedir confirmação do usuário |

#### US33 - Encaminhar notícia

| **US33** | **Encaminhar notícia**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Encaminhar notícia |
| **Para que eu possa** | Compartilhar uma notícias com outros usuários do app |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve filtrar usuários <br> > Deve permitir enviar para mais um usuário por vez |

## EP15 - Chat

#### US35 - Visualizar conversas

| **US35** | **Visualizar conversas**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar conversas |
| **Para que eu possa** | Acessar conversas com outros usuários |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve mostrar em ordem de mais recentes <br> > Deve sinalizar conversas nao lidas <br> Deve mostrar horário e remetente da mensagem <br> Deve filtrar conversas por nome do remetente |

#### US36 - Visualizar contatos

| **US36** | **Visualizar contatos**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Visualizar contatos |
| **Para que eu possa** | Selecionar contato para iniciar uma conversa |
| **Pontos** | 5 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve listar todos os usuários disponíveis <br> Deve filtrar contatos por nome |

#### US37 - Apagar conversas

| **US37** | **Apagar conversas**|
|--|--|
| **Versão**| Atual: 1.0 (10/06) <br> Anterior: --|
| **Eu, como** | Usuário |
|**Desejo** | Apagar conversas |
| **Para que eu possa** | Desabilitar mensagens que não desejo ver |
| **Pontos** | 2 |
| **Prioridade** | Must |
| **Critérios de aceitação** | > Deve pedir confirmação do usuário |


















