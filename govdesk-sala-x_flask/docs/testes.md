# CRITÉRIOS DE ACEITE DE TESTE

## TESTES DE CADASTRO DE USUÁRIO

| CRITÉRIO DE ACEITE | DESCRIÇÃO / REQUISITO |
| :--- | :--- |
| **CRITÉRIO 1** | Ao cadastrar o CPF deve ter um cálculo para validar se os números estão corretos e correspondem ao de CPF. |
| **CRITÉRIO 2** | Ao digitar o campo telefone não deve ser permitido o dígito de strings ou caracteres e que tenha o limite correto de números de telefone (9 dígitos). |
| **CRITÉRIO 3** | Após digitar o email e senha deve aparecer a tela de verificador de dois passos. |
| **CRITÉRIO 4** | Para o cadastro ser efetivado é necessário o email ou telefone para verificação e segurança da conta, além de CPF para a identificação do usuário. |
| **CRITÉRIO 5** | Após o cadastro ser efetuado com sucesso deve redirecionar para a página de usuário. |
| **CRITÉRIO 6** | Ao solicitar chamada deve descrever o problema ou enviar arquivos do problema e toda vez que for criada uma chamada deve classificar o tipo de problema se é software, hardware, rede, projetor ou acesso. |
| **CRITÉRIO 7** | Assim que o professor ou aluno for finalizar a chamada no sistema da equipe de TI deve aparecer na notificação e na tela de chamadas. |

---

## TESTE AO CRIAR CHAMADAS

| CRITÉRIO DE ACEITE | DESCRIÇÃO / REQUISITO |
| :--- | :--- |
| **CRITÉRIO 1** | O usuário após finalizar a chamada deve aparecer na tela que foi encaminhado a solicitação. |
| **CRITÉRIO 2** | Todas as solicitações devem ser enviadas e, após a finalização, o usuário deve ser redirecionado para a página que verifica o status da chamada. |
| **CRITÉRIO 3** | No exato momento em que o chamado for criado, o sistema deve gerar automaticamente um identificador único (ID/Número do Protocolo) para servir como chave de busca e rastreamento. |
| **CRITÉRIO 4** | O sistema deve impedir a criação de chamadas que tenham o campo de descrição ou assunto em branco, exibindo o alerta: "Por favor, descreva o problema enfrentado antes de enviar". |
| **CRITÉRIO 5** | O formulário deve exibir um botão "Cancelar" ao lado do botão "Enviar". Se o usuário clicar nele, o sistema deve limpar todos os campos digitados e voltar para o Dashboard sem criar nenhum chamado. |

---

## TESTE AO FAZER LOGIN

| CRITÉRIO DE ACEITE | DESCRIÇÃO / REQUISITO |
| :--- | :--- |
| **CRITÉRIO 1** | O sistema deve validar as credenciais digitadas. Se o e-mail ou a senha estiverem incorretos, deve impedir o acesso e exibir a mensagem genérica: "E-mail ou senha inválidos". |
| **CRITÉRIO 2** | O campo de senha deve ocultar os caracteres digitados por meio de bolinhas ou asteriscos, possuindo um ícone de "olho" para que o usuário possa alternar e visualizar a senha se desejar. |
| **CRITÉRIO 3** | Após digitar o email e senha e estiver correto deve seguir uma tela de verificador de dois passos. |
| **CRITÉRIO 4** | Os campos de E-mail e Senha devem ser validados antes do envio. Se o usuário clicar em "Entrar" com algum dos dois campos vazios, o sistema deve destacar o campo em vermelho e exibir: "Campo obrigatório". |
| **CRITÉRIO 5** | Ao clicar em "Esqueci minha senha", o sistema deve redirecioná-lo para uma nova tela contendo um campo para preenchimento de e-mail e o botão "Enviar link de recuperação". |
| **CRITÉRIO 6** | O sistema deve bloquear temporariamente o login por 15 minutos se o usuário errar a senha 5 vezes seguidas, exibindo a mensagem: "Conta bloqueada por excesso de tentativas". |
| **CRITÉRIO 7** | Após passar pelo login e pela verificação de dois passos, o sistema deve identificar o perfil da conta e redirecionar o Técnico de TI para o painel de atendimento e o Usuário Comum para o histórico de chamadas. |

---

## TESTE AO RESPONDER CHAMADAS (VISÃO DO TÉCNICO)

| CRITÉRIO DE ACEITE | DESCRIÇÃO / REQUISITO |
| :--- | :--- |
| **CRITÉRIO 1** | O painel do técnico deve permitir o anexo de arquivos ou fotos (ex: foto da peça trocada ou print de configuração) de até 5MB como comprovação do serviço realizado. |
| **CRITÉRIO 2** | Toda vez que o técnico enviar uma resposta ou comentário no chamado, o sistema deve enviar uma notificação em tempo real no sistema ou e-mail para que o professor ou aluno que abriu a solicitação veja. |
| **CRITÉRIO 3** | O sistema deve possuir uma opção de "Nota Interna" (visível apenas para a equipe de TI). O usuário comum (professor/aluno) não poderá visualizar os comentários marcados com esse tipo de privacidade. (Serve para grupos de TI criarem uma tarefa para direcionar a responsabilidade para fazer a tarefa). |
| **CRITÉRIO 4** | O sistema deve salvar automaticamente a assinatura do técnico (nome e cargo) e a marca de tempo (data/hora) em cada mensagem enviada, criando uma linha do tempo imutável para auditoria. |
| **CRITÉRIO 5** | Quando a tarefa/chamada for marcada como concluída pelo técnico, ela deve sair automaticamente do campo de afazeres ativos do painel. |
| **CRITÉRIO 6** | O técnico deve conseguir alterar o status do chamado para "Aguardando Usuário" caso precise de mais informações do professor/aluno. Esse status deve destacar o chamado com uma cor diferente no painel e pausar temporariamente a contagem do tempo de atendimento. |
| **CRITÉRIO 7** | O sistema deve calcular automaticamente o tempo total decorrido entre a abertura do chamado pelo usuário e a resposta final do técnico, salvando esse dado no histórico para fins de relatório de desempenho da TI. |