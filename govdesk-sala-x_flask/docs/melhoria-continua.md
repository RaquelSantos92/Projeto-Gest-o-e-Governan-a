# Plano de Melhoria Contínua — Sistema de Chamados FATEC-PG

## 1. Não conformidades

| ID | Achado | Requisito violado | Evidência | Gravidade |
|----|--------|-------------------|-----------|-----------|
| NC1 | Há divergência na grafia do nome de um integrante entre os documentos do projeto. | Padronização e consistência da documentação do projeto. | Na matriz RACI e na solicitação de mudança consta “Felipe”, enquanto no backlog e na EAP consta “Fellipe”. | Baixa |
| NC2 | O tratamento de imagens anexadas aos chamados não foi incluído no inventário de dados pessoais. | Documento LGPD; princípios de finalidade, adequação e necessidade previstos no art. 6º da LGPD. | A US01 prevê a possibilidade de anexar pelo menos uma imagem/foto do problema, mas a tabela LGPD não registra esse dado ou arquivo. | Alta |
| NC3 | O prazo de retenção de 24 meses foi definido para todos os dados sem apresentar justificativa ou procedimento de descarte. | Documento LGPD; princípios da necessidade e da segurança, previstos no art. 6º da LGPD, e regras de término do tratamento do art. 15. | A coluna “Retenção” apresenta “24 meses” para todos os registros, sem indicar o critério de definição do prazo ou o procedimento após seu encerramento. | Média |
| NC4 | A prioridade pode ser selecionada pelo solicitante, mas não há critérios objetivos para orientar essa escolha ou permitir sua revisão pela equipe de suporte. | PETI e backlog do produto, especialmente US01 e US05; necessidade de critérios consistentes para classificação e triagem. | US01 prevê campo de prioridade para seleção do usuário; US05 prevê ordenação por prioridade, mas não define níveis, critérios de classificação ou validação pela equipe. | Média |
| NC5 | Os papéis operacionais citados no backlog não estão representados na matriz RACI. | Matriz RACI e backlog do produto; definição clara de responsabilidades. | US04 cita técnico de laboratório/suporte; US05 cita coordenador de TI/Suporte; US06 cita gestor. A RACI apresenta apenas Product Owner, Dev Leads e QA. | Média |

## 2. Causa raiz (5 Porquês)

**NC2: Imagens anexadas não incluídas no inventário LGPD**

1. Por quê? Porque as imagens previstas no formulário de abertura de chamados não foram registradas na tabela LGPD.
2. Por quê? Porque o levantamento dos dados considerou principalmente os campos textuais, sem detalhar os arquivos anexados.
3. Por quê? Porque o backlog e o documento LGPD foram elaborados sem uma conferência cruzada entre as funcionalidades e os dados tratados.
4. Por quê? Porque os critérios de aceite das histórias não exigem a verificação dos dados envolvidos em cada funcionalidade.
5. Por quê? Porque a análise de privacidade ainda não está incorporada formalmente ao processo de definição e validação dos requisitos.

**Causa raiz:** falta de integração entre o levantamento de requisitos funcionais e o inventário dos dados tratados pelo sistema.

**NC4: Ausência de critérios objetivos para a prioridade dos chamados**

1. Por quê? Porque o solicitante pode selecionar a prioridade sem orientação sobre os critérios de classificação.
2. Por quê? Porque o backlog prevê o campo de prioridade, mas não descreve níveis ou condições para cada classificação.
3. Por quê? Porque a necessidade de ordenar os chamados foi tratada como requisito funcional, sem detalhar as regras operacionais de triagem.
4. Por quê? Porque não foi definida uma etapa de validação das regras de prioridade com os responsáveis pelo atendimento.
5. Por quê? Porque o processo de levantamento de requisitos não estabeleceu critérios de aceite específicos para a classificação e revisão da prioridade.

**Causa raiz:** ausência de regras operacionais formalizadas e validadas para classificar e revisar a prioridade dos chamados.

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
| Gestão de chamados e atendimento | 2 — Repetível | 4 — Gerenciado | O backlog descreve abertura, acompanhamento, atendimento, triagem e relatórios. Entretanto, não foram apresentados registros de execução ou indicadores históricos que comprovem a padronização e o controle do processo. |
| Gestão de privacidade e dados pessoais | 1 — Inicial | 3 — Definido | Existe uma tabela LGPD, mas os anexos previstos no backlog não estão inventariados e o prazo de retenção de 24 meses não apresenta justificativa ou procedimento de descarte. |
| Gestão de mudanças e desenvolvimento | 2 — Repetível | 3 — Definido | O projeto possui RACI, backlog, solicitação de mudança e EAP, mas não foram apresentados registros de execução do fluxo, commits ou evidências de testes que demonstrem sua aplicação contínua. |

## 5. Plano 5W2H

| O quê | Por quê | Onde | Quem | Quando | Como | Custo | Tipo (QW/Projeto) | NC |
|-------|---------|-------|------|--------|------|-------|-------------------|----|
| Padronizar a grafia do nome do integrante nos documentos do projeto. | Evitar divergências de identificação e manter a documentação consistente. | Documentos do projeto: RACI, backlog, EAP e solicitação de mudança. | João (PO) e equipe. | Sprint 3 | Conferir os documentos e aplicar a grafia correta e única do nome em todos os registros. | R$ 0,00 | QW | NC1 |
| Incluir imagens e anexos no inventário LGPD. | Documentar todos os dados previstos nas funcionalidades do sistema e estabelecer os cuidados aplicáveis aos arquivos enviados. | Tabela LGPD e documentação da US01. | Raquel (QA) e Alan (QA), com apoio dos Dev Leads. | Sprint 3 | Atualizar a tabela LGPD com a descrição dos anexos, finalidade, perfis de acesso, retenção e procedimento de descarte a definir. | R$ 0,00 | QW | NC2 |
| Definir critérios objetivos de prioridade dos chamados. | Evitar classificações inconsistentes e organizar a fila de atendimento. | Backlog do produto, requisitos da US01 e US05 e fluxo de atendimento. | João (PO), Emanuel e Fellipe (Dev Leads). | Sprint 3 | Definir níveis de prioridade, critérios de classificação e regras para revisão pela equipe de suporte; registrar os critérios no backlog. | R$ 0,00 | QW | NC4 |
| Incluir os papéis operacionais na matriz RACI. | Esclarecer as responsabilidades de técnicos, coordenação e gestão durante o atendimento. | Matriz RACI e documentação dos requisitos US04, US05 e US06. | João (PO) e equipe. | Fase 2 | Revisar a matriz e incluir as atividades e os papéis operacionais, mantendo um único responsável “A” por atividade. | R$ 0,00 | Projeto | NC5 |
| Definir critérios de retenção e descarte por categoria de dado. | Justificar os prazos de armazenamento e evitar retenção sem necessidade. | Tabela LGPD e documentação institucional aplicável. | João (PO), QA e responsável institucional. | Fase 2 | Consultar as regras institucionais, documentar os prazos aplicáveis por categoria de dado e definir o procedimento de descarte. | A definir após validação institucional. | Projeto | NC3 |

## 6. Roadmap

**Fase 1 (0–30 dias):** executar os quick wins previstos para a Sprint 3: padronizar a grafia do nome do integrante nos documentos (NC1), incluir imagens e anexos no inventário LGPD (NC2) e definir critérios objetivos para a prioridade dos chamados (NC4).

**Fase 2 (1–3 meses):** revisar a matriz RACI para contemplar os papéis operacionais de atendimento (NC5) e definir critérios de retenção e descarte dos dados, considerando as orientações institucionais aplicáveis (NC3).

**Fase 3 (3–6 meses):** acompanhar os indicadores do BSC com dados reais do sistema, avaliar o cumprimento das metas e revisar os processos de atendimento, desenvolvimento e privacidade com base nos resultados obtidos.
