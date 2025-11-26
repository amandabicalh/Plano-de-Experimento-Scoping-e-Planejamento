# Plano de Experimento — Seções 1 a 6 

## 1. Identificação básica

### 1.1 Título do experimento

**Impacto do uso de checklist estruturado em revisões de código (pull requests) sobre a detecção de defeitos e o tempo de revisão**

*Justificativa do título:* título claro e descritivo que informa o que será comparado (revisão de código com checklist estruturado vs. revisão de código sem checklist), quais resultados serão medidos (detecção de defeitos e tempo de revisão) e o contexto operacional (pull requests / revisões em repositórios de software).

### 1.2 ID / código

**TCC-EXP-ENGSW-2025-001**

### 1.3 Versão do documento e histórico de revisão

- **Versão:** v1.0  
- **Histórico de revisão:**  
  - v1.0 (2025-11-21) — Criação inicial do plano com Seções 1 e 2 concluídas.

### 1.4 Datas (criação, última atualização)

- **Data de criação:** 21 de novembro de 2025  
- **Data da última atualização:** 21 de novembro de 2025

### 1.5 Autores (nome, área, contato)

- **Amanda Bicalho Silva** — Engenharia de Software (graduanda).  
  Contato: *amanda.bicalho@sga.pucminas.br*.  
- Orientador(a) / coautor(a) — Danilo de Quadros Maia Filho.

### 1.6 Responsável principal (PI / dono do experimento)

- **Amanda Bicalho Silva** — estudante responsável pelo desenho e execução do experimento.

### 1.7 Projeto / produto / iniciativa relacionada

- **Projeto/Disciplina:** Trabalho Final da disciplina Medição e Experimentação em Engenharia de Software — Curso de Engenharia de Software, PUC Minas.
- **Conexão com iniciativas:** possível integração com repositório do TCC, projetos de extensão ou equipe júnior.

---

## 2. Contexto e problema

### 2.1 Descrição do problema / oportunidade

**Problema:**  
Revisões de código são fundamentais para detectar defeitos e melhorar qualidade, mas revisões informais e não estruturadas apresentam grande variabilidade, com revisores esquecendo itens importantes, focando apenas em estilo, deixando passar defeitos ou gastando mais tempo que o necessário.

**Oportunidade:**  
Um checklist estruturado pode padronizar o processo, aumentar a taxa de detecção de defeitos relevantes e reduzir o tempo de revisão. É uma intervenção simples, de baixo custo e adequada tanto ao ambiente acadêmico quanto profissional.

**Sinais observados (motivação prática):**

- Comentários repetitivos em vários PRs.
- Bugs descobertos em testes que passaram despercebidos pelo revisor.
- Revisões demoradas, atrasando merges.

**Impacto esperado:**  
Melhor detecção precoce de defeitos, redução de retrabalho e padronização do processo de revisão.

### 2.2 Contexto organizacional e técnico

**Ambiente proposto:**

- **Cenário:** ambiente acadêmico (disciplina de Engenharia de Software) ou equipe pequena de desenvolvimento.
- **Participantes:** desenvolvedores/estudantes com experiência básica em Git/GitHub/GitLab.
- **Ferramentas:** Git, GitHub/GitLab, diffs, PR logs, planilhas e formulários de coleta.
- **Processo:** feature branches, pull requests e revisões manuais peer review.
- **Restrições:** não usar ferramentas automatizadas que substituam itens do checklist.
- **Modo de execução:** revisões assíncronas (48h) ou sessões controladas presenciais.

### 2.3 Trabalhos e evidências prévias (internos e externos)

**Evidências internas:**

- Histórico de PRs em projetos acadêmicos.
- Observação de variação na qualidade das revisões entre alunos.

**Evidências externas:**

- Estudos clássicos de inspeção de software (ex.: Fagan).
- Pesquisas que mostram que checklists aumentam eficácia em inspeções.
- Trabalhos sobre práticas de code review, variabilidade entre revisores e carga cognitiva.

### 2.4 Referencial teórico e empírico essencial

1. **Inspeção estruturada e checklists:** ajudam a padronizar observações e reduzir erros de omissão.
2. **Variabilidade humana e carga cognitiva:** checklists reduzem carga mental e aumentam profundidade da análise.
3. **Economia do defeito:** defeitos descobertos cedo têm menor custo.
4. **Métricas de revisão:** taxa de detecção de defeitos, tempo de revisão, número de comentários, reabertura de PRs.
5. **Validade e generalização:** efeitos do checklist podem variar conforme experiência do revisor e complexidade do código.

---


# 3. Objetivos e Questões (Goal / Question / Metric)

## 3.1 Objetivo Geral (Goal Template)

Analyze **o uso de um checklist estruturado para code review**  
for the purpose of **avaliar sua eficácia na melhoria da qualidade da revisão de código**  
with respect to **precisão, completude, padronização e eficiência**  
from the point of view of **revisores, desenvolvedores e líderes técnicos**  
in the context of **projetos de software acadêmicos e profissionais com equipes de diferentes níveis de experiência**.

---

## 3.2 Objetivos Específicos

- **O1.** Avaliar se o checklist aumenta a precisão da identificação de defeitos durante o code review.  
- **O2.** Avaliar se o checklist melhora a completude da revisão, reduzindo itens não verificados.  
- **O3.** Avaliar o impacto do checklist no tempo da revisão e na necessidade de retrabalho.  
- **O4.** Avaliar a percepção dos revisores quanto à utilidade e facilidade de uso do checklist.  
- **O5.** Comparar a consistência entre diferentes revisores utilizando o checklist.

---

## 3.3 Questões de Pesquisa / de Negócio

- **Q1.** O checklist aumenta o número de defeitos reais identificados?  
- **Q2.** O checklist reduz falsos positivos?  
- **Q3.** Revisões feitas com checklist cobrem mais itens essenciais?  
- **Q4.** Revisores deixam menos itens sem verificação ao usar checklist?  
- **Q5.** O checklist aumenta ou reduz o tempo total da revisão?  
- **Q6.** O checklist reduz a necessidade de revisões adicionais?  
- **Q7.** O checklist é considerado útil pelos revisores?  
- **Q8.** O checklist facilita a tomada de decisão e aumenta a confiança dos revisores?  
- **Q9.** Revisores diferentes produzem resultados mais consistentes quando usam o checklist?

---

## 3.4 Métricas Associadas (GQM)

### Tabela GQM — Métricas por Pergunta

| Questão | Métricas                    | Definição                                    | Unidade    | Fonte                    |
| ------- | --------------------------- | -------------------------------------------- | ---------- | ------------------------ |
| Q1      | M1: Defeitos verdadeiros    | Número de defeitos reais encontrados         | Contagem   | Logs de revisão          |
| Q1      | M3: Defeitos críticos (%)   | Proporção de defeitos críticos               | %          | Análise de severidade    |
| Q2      | M2: Falsos positivos        | Problemas sinalizados incorretamente         | Contagem   | Logs de revisão          |
| Q3      | M4: Cobertura de itens (%)  | Percentual de itens do checklist verificados | %          | Checklist preenchido     |
| Q4      | M5: Itens ignorados         | Itens não verificados                        | Contagem   | Checklist preenchido     |
| Q5      | M6: Tempo total             | Tempo gasto para concluir o review           | Minutos    | Ferramenta de tracking   |
| Q6      | M7: Revisões adicionais     | Número de revisões extras                    | Contagem   | Histórico de tarefas     |
| Q7      | M8: Nota de utilidade       | Avaliação subjetiva dos revisores            | Escala 1–5 | Questionário             |
| Q8      | M9: Índice de confiança     | Percepção de segurança na decisão            | Escala 1–5 | Questionário             |
| Q9      | M10: Índice de consistência | Similaridade entre revisores                 | %          | Comparação entre reviews |

---

# 4. Escopo e Contexto do Experimento

## 4.1 Escopo Funcional / de Processo (Incluído e Excluído)

### **Incluído**
- Processo de *code review* aplicado ao módulo X do projeto.  
- Uso de checklist estruturado para validação do código.  
- Participação de revisores com diferentes níveis de experiência.  
- Coleta de dados de tempo, defeitos e percepções.

### **Excluído**
- Alterações no processo de desenvolvimento como um todo.  
- Avaliação de performance do sistema.  
- Intervenção no código além da revisão.  
- Revisões automatizadas por ferramentas estáticas.

---

## 4.2 Contexto do Estudo

- **Tipo de organização:** ambiente acadêmico/profissional híbrido.  
- **Projeto:** sistema modular de médio porte com requisitos estáveis.  
- **Tamanho da equipe:** 6 a 10 participantes.  
- **Experiência dos participantes:** intermediária, com conhecimento prévio de Git e revisão de código.  
- **Criticidade:** média — impacto moderado caso defeitos passem.

---

## 4.3 Premissas

- Checklist estará disponível e acessível para todos.  
- Participantes seguirão o checklist corretamente.  
- Ambiente de desenvolvimento permanecerá estável.  
- Tempo suficiente será alocado para realização das revisões.

---

## 4.4 Restrições

- Janela limitada de tempo para execução.  
- Ferramentas obrigatórias definidas pela organização.  
- Participantes podem ter cargas de trabalho variáveis.  
- Não é possível expandir o tamanho da amostra.

---

## 4.5 Limitações Previstas

- Diferença de experiência pode impactar resultados.  
- Resultados podem não generalizar para equipes grandes.  
- Checklist analisado pode não ser adequado para todo tipo de projeto.  
- Amostra pode ser pequena para conclusões estatísticas amplas.

---

# 5. Stakeholders e Impacto Esperado

## 5.1 Stakeholders Principais

- Desenvolvedores  
- Revisores  
- QA  
- Gerentes técnicos / Tech Leads  
- Equipe de produto  

---

## 5.2 Interesses e Expectativas dos Stakeholders

- **Desenvolvedores:** receber feedback mais útil e padronizado.  
- **Revisores:** ter maior apoio na identificação de problemas.  
- **QA:** redução de defeitos em testes.  
- **Gestores:** maior eficiência, menos retrabalho e previsibilidade.  
- **Produto:** melhoria de qualidade percebida.

---

## 5.3 Impactos Potenciais no Processo / Produto

- Possível aumento inicial no tempo de revisão.  
- Redução de bugs em versões posteriores.  
- Padronização do processo de review.  
- Aumento de carga para revisores menos experientes.

---

# 6. Riscos de Alto Nível, Premissas e Critérios de Sucesso

## 6.1 Riscos de Alto Nível

- Inconsistência no uso do checklist.  
- Falta de disponibilidade dos participantes.  
- Perda de dados por falha de ferramenta.  
- Resistência cultural ao uso do checklist.  
- Qualidade do código analisado variar demais.

---

## 6.2 Critérios de Sucesso Globais (Go / No-Go)

- Pelo menos **80% de adesão** ao checklist.  
- **Aumento de 20%** na identificação de defeitos reais.  
- Redução de falsos positivos.  
- Alta percepção de utilidade (**média ≥ 4**).

---

## 6.3 Critérios de Parada Antecipada

- Indisponibilidade de participantes-chave.  
- Falha crítica no ambiente de desenvolvimento.  
- Cancelamento do projeto ou mudança completa de escopo.  
- Identificação de viés severo que invalide o experimento.


```md
