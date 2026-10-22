
# 📋 Backlog do Produto - Sistema de Chamados (FATEC-PG)

Este documento descreve o backlog inicial do sistema de gerenciamento de chamados técnicos e operacionais para a **FATEC Praia Grande**, atendendo discentes, docentes e a equipe de suporte/infraestrutura.

---

## 🏛️ Épico 1: Abertura e Acompanhamento de Chamados (Comunidade Acadêmica)
Focado na experiência dos alunos, professores e funcionários para submeter e acompanhar demandas (infraestrutura, laboratórios de informática, secretaria e TI).

---

### US01 - Abertura de chamado de infraestrutura/TI
- **História:** Como **aluno ou professor da FATEC-PG**, quero **abrir um chamado especificando categoria, local (ex: Lab 03) e descrição do problema**, para **notificar a equipe de suporte sobre falhas nos equipamentos ou instalações**.
- **Critérios de Aceite:**
  - [ ] O usuário deve selecionar obrigatoriamente: Categoria (Hardware, Software, Rede, Estrutura), Bloco/Sala e Descrição.
  - [ ] Possibilidade de anexar ao menos 1 imagem/foto do problema.
  - [ ] O sistema gera um número de protocolo único após o envio.
  - [ ] Campo de prioridade para seleção do usuário.
- **Prioridade:** Alta
- **Responsável:** Dev Lead (Emanuel)
- **Sprint:** Sprint 1

---

### US02 - Consulta e acompanhamento de status do chamado
- **História:** Como **solicitante**, quero **visualizar uma lista com o status atualizado dos meus chamados abertos**, para **saber se meu problema já está em atendimento ou foi resolvido**.
- **Critérios de Aceite:**
  - [ ] Listar chamados com badges de status: `Aberto`, `Em Atendimento`, `Aguardando Peça`, `Concluído` e `Cancelado`.
  - [ ] Permitir filtrar chamados por status e data de abertura.
  - [ ] Exibir histórico resumido de alterações de status.
- **Prioridade:** Alta
- **Responsável:** Dev Lead (Emanuel)
- **Sprint:** Sprint 1

---

### US03 - Notificações de atualização por e-mail institucional
- **História:** Como **usuário com e-mail institucional (@fatec.sp.gov.br)**, quero **receber notificações automáticas a cada mudança de status do meu chamado**, para **ficar informado sem precisar acessar a plataforma a todo momento**.
- **Critérios de Aceite:**
  - [ ] Disparo de e-mail ao criar o chamado com o número de protocolo.
  - [ ] Disparo de e-mail quando o status mudar para `Em Atendimento` e `Concluído`.
  - [ ] O e-mail deve conter link direto para os detalhes do chamado.
- **Prioridade:** Baixa
- **Responsável:** Dev Lead (Emanuel)
- **Sprint:** Sprint 2

---

## 🛠️ Épico 2: Gestão, Triagem e Resolução (Equipe de Suporte e TI)
Focado no fluxo de trabalho dos técnicos de TI, manutenção predial e coordenação da FATEC-PG.

---

### US04 - Atribuição e atendimento de chamado pelo técnico
- **História:** Como **técnico do laboratório/suporte da FATEC-PG**, quero **assumir um chamado da fila e registrar pareceres técnicos**, para **informar o andamento da manutenção e manter o histórico do serviço**.
- **Critérios de Aceite:**
  - [ ] Botão "Assumir Chamado" que vincula o técnico autenticado à solicitação.
  - [ ] Campo de texto para adicionar notas técnicas e solução aplicada.
  - [ ] Apenas administradores ou técnicos atribuídos podem alterar o status do chamado.
- **Prioridade:** Alta
- **Responsável:** Dev Lead (Fellipe)
- **Sprint:** Sprint 2

---

### US05 - Filtragem e priorização da fila de atendimento
- **História:** Como **coordenador de TI/Suporte**, quero **classificar e ordenar os chamados por urgência e local**, para **garantir que problemas críticos (ex: laboratório sem rede durante aula) sejam atendidos primeiro**.
- **Critérios de Aceite:**
  - [ ] Ordenação da fila por prioridade decrescente e data de abertura.
  - [ ] Alerta visual para chamados sem atendimento há mais de 48 horas úteis.
- **Prioridade:** Baixa
- **Responsável:** Dev Lead (Fellipe)
- **Sprint:** Sprint 3

---

### US06 - Relatório gerencial de atendimentos da unidade
- **História:** Como **diretor de serviços ou gestor da FATEC-PG**, quero **visualizar métricas de chamados atendidos, tempo médio de resolução e locais mais problemáticos**, para **tomar decisões sobre compra de insumos e melhorias estruturais**.
- **Critérios de Aceite:**
  - [ ] Gráfico com total de chamados abertos vs. fechados por mês.
  - [ ] Indicador de tempo médio de atendimento (SLA).
  - [ ] Exportação dos dados filtrados em formato `.CSV` ou `.PDF`.
- **Prioridade:** Baixa
- **Responsável:** Dev Lead (Fellipe)
- **Sprint:** Sprint 3