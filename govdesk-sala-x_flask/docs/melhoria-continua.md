# Plano de Melhoria Contínua — Sistema de Chamados FATEC-PG

## 1. Não conformidades

| ID | Achado | Requisito violado | Evidência | Gravidade |
|----|--------|-------------------|-----------|-----------|
| NC1 | A base legal “Contrato” foi atribuída indistintamente a todos os dados pessoais, sem justificativa específica para o contexto da Fatec Praia Grande. | Documento LGPD; LGPD, arts. 6º e 7º (princípios do tratamento e hipóteses legais). | Na tabela LGPD, a coluna “Base legal” apresenta “Contrato” para todos os dados, embora o escopo tenha sido alterado de uma empresa fictícia para uma instituição de ensino. | Alta |
| NC2 | O tratamento de imagens anexadas aos chamados não foi incluído no inventário de dados pessoais. | Documento LGPD; LGPD, arts. 6º e 7º. | US01, nos critérios de aceite, prevê a possibilidade de anexar pelo menos uma imagem/foto do problema, mas a tabela LGPD não registra esse dado. | Alta |
| NC3 | O prazo de retenção de 24 meses foi definido para todos os dados sem apresentar justificativa ou procedimento de descarte. | Documento LGPD; LGPD, art. 6º, III, e art. 15. | A coluna “Retenção” apresenta “24 meses” para todos os registros, sem indicar critério de definição ou o que ocorre após o prazo. | Média |
| NC4 | A prioridade pode ser selecionada pelo solicitante, mas não há critérios objetivos para orientar essa escolha ou permitir sua revisão pela equipe de suporte. | PETI e backlog do produto, especialmente US01 e US05. | US01 prevê “Campo de prioridade para seleção do usuário”; US05 prevê ordenação por prioridade, mas não define níveis, critérios ou validação. | Média |
| NC5 | Os papéis operacionais citados no backlog não estão representados na matriz RACI. | Matriz RACI e backlog do produto; definição clara de responsabilidades. | US04 cita técnico de laboratório/suporte; US05 cita coordenador de TI/Suporte; US06 cita gestor. A RACI apresenta apenas Product Owner, Dev Leads e QA. | Média |

## 2. Causa raiz (5 Porquês)

**NC1: Base legal genérica para todos os dados**

1. Por quê? Porque “Contrato” foi utilizado como base legal para todos os dados.
2. Por quê? Porque o documento foi preenchido com uma hipótese genérica, sem diferenciar as finalidades e o contexto de cada tratamento.
3. Por quê? Porque a alteração do escopo, de uma empresa fictícia para a Fatec Praia Grande, não foi acompanhada de uma revisão completa da tabela LGPD.
4. Por quê? Porque não foi estabelecida uma etapa obrigatória de revisão de privacidade quando o escopo ou os requisitos são alterados.
5. Por quê? Porque o processo de gestão documental do projeto ainda não possui um checklist específico de validação LGPD.

**Causa raiz:** ausência de um procedimento de revisão de privacidade que considere o contexto institucional e valide as hipóteses legais aplicáveis.

**NC2: Imagens anexadas não incluídas no inventário LGPD**

1. Por quê? Porque as imagens previstas no formulário não foram registradas na tabela LGPD.
2. Por quê? Porque o levantamento dos dados considerou os campos textuais, mas não os arquivos anexados.
3. Por quê? Porque o backlog e o documento LGPD foram elaborados sem uma conferência cruzada.
4. Por quê? Porque os critérios de aceite das histórias não exigem a verificação dos dados tratados pela funcionalidade.
5. Por quê? Porque a privacidade ainda não está incorporada formalmente ao processo de definição e validação dos requisitos.

**Causa raiz:** falta de integração entre o levantamento de requisitos funcionais e o inventário dos dados tratados pelo sistema.

## 3. BSC

| Perspectiva | Objetivo | Indicador | Meta | Iniciativa | Dono |
|-------------|----------|-----------|------|------------|------|
| Financeira | Reduzir o tempo desperdiçado com solicitações de suporte desorganizadas. | Variação do tempo médio entre a abertura e a conclusão dos chamados. | Reduzir em 20% até o fim do semestre, após estabelecer a linha de base. | Centralizar as solicitações e acompanhar mensalmente o tempo de atendimento. | João (Product Owner) |
| Clientes | Melhorar a satisfação de alunos, professores e funcionários com o atendimento. | Média das avaliações dos solicitantes após a conclusão dos chamados, em escala de 1 a 5. | Alcançar média igual ou superior a 4,0 até o fim do semestre. | Disponibilizar acompanhamento do chamado e avaliação após o atendimento. | João (Product Owner) |
| Processos | Garantir que as solicitações recebidas sejam registradas e rastreáveis. | Percentual de solicitações registradas no sistema em relação ao total recebido nos canais contemplados. | Registrar 100% das solicitações abrangidas pelo projeto até o fim do semestre. | Implantar protocolo único, histórico de status e rotina de triagem. | João (Product Owner) |
| Aprendizado | Melhorar a qualidade das entregas de desenvolvimento e testes. | Percentual de entregas concluídas com revisão e evidência de teste. | Ter 100% das entregas da Sprint 3 revisadas e testadas. | Utilizar checklist de revisão, versionamento e registro dos testes. | João (Product Owner) |

## 4. Maturidade (0 a 5)

| Processo | Atual | Alvo | Evidência |
|----------|-------|------|-----------|
| Gestão de chamados e atendimento | 2 — Repetível | 4 — Gerenciado | O backlog descreve abertura, acompanhamento, atendimento, triagem e relatórios. Entretanto, não foram apresentados registros de execução ou indicadores históricos. |
| Gestão de privacidade e dados pessoais | 1 — Inicial | 3 — Definido | Existe uma tabela LGPD, mas a base legal é genérica e os anexos previstos no backlog não estão inventariados. |
| Gestão de mudanças e desenvolvimento | 2 — Repetível | 3 — Definido | O projeto possui RACI, backlog, solicitação de mudança e EAP, mas não foram apresentados registros de execução do fluxo, commits ou evidências de testes. |

## 5. Plano 5W2H

| O quê | Por quê | Quem | Quando | Como | Custo | Tipo (QW/Projeto) | NC |
|-------|---------|------|--------|------|-------|-------------------|----|
| Revisar a base legal e as finalidades da tabela LGPD. | Adequar o documento ao contexto da Fatec e evitar o uso de uma hipótese legal genérica. | João (PO), com validação institucional. | Sprint 3 | Revisar a finalidade de cada dado e encaminhar as hipóteses legais para validação institucional. | R$ 0,00 (equipe acadêmica; validação interna). | QW | NC1 |
| Incluir imagens e anexos no inventário LGPD. | Documentar todos os dados previstos nas funcionalidades do sistema. | Raquel (QA) e Alan (QA), com apoio dos Dev Leads. | Sprint 3 | Atualizar a tabela LGPD com finalidade, acesso, retenção e descarte dos anexos. | R$ 0,00 | QW | NC2 |
| Definir critérios objetivos de prioridade dos chamados. | Evitar classificações inconsistentes e organizar a fila de atendimento. | João (PO), Emanuel e Felipe/Fellipe (Dev Leads). | Sprint 3 | Definir níveis de prioridade, critérios de classificação e regras para revisão pela equipe de suporte. | R$ 0,00 | QW | NC4 |
| Incluir os papéis operacionais na matriz RACI. | Esclarecer as responsabilidades de técnicos, coordenação e gestão. | João (PO) e equipe. | Fase 2 | Revisar a matriz e incluir as atividades operacionais, mantendo um único responsável “A” por atividade. | R$ 0,00 | Projeto | NC5 |
| Definir critérios de retenção e descarte por categoria de dado. | Justificar os prazos de armazenamento e evitar retenção sem necessidade. | João (PO), QA e responsável institucional. | Fase 2 | Consultar as regras institucionais, documentar os prazos aplicáveis e definir o procedimento de descarte. | A definir após validação institucional. | Projeto | NC3 |

## 6. Roadmap

**Fase 1 (0–30 dias):** executar os quick wins da Sprint 3: revisar a base legal e as finalidades da tabela LGPD (NC1), incluir imagens e anexos no inventário (NC2) e definir critérios de prioridade dos chamados (NC4). Padronizar também os documentos após confirmar os nomes dos integrantes responsáveis.

**Fase 2 (1–3 meses):** revisar a matriz RACI para contemplar os papéis operacionais (NC5) e definir critérios de retenção e descarte dos dados (NC3), considerando as orientações institucionais aplicáveis.

**Fase 3 (3–6 meses):** acompanhar os indicadores do BSC com dados reais do sistema, avaliar o cumprimento das metas e revisar os processos de atendimento e privacidade com base nos resultados obtidos.