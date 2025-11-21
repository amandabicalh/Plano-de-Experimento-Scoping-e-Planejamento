# Plano de Experimento — Seções 1 e 2 

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

*Fim das Seções 1 e 2.*

```md
