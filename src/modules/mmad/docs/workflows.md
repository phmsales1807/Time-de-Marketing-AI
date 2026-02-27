# Workflows Reference

mmad includes 14 workflows organized by category:

---

## Core Workflows

### Brand Brief

**Purpose:** Facilitar a descoberta do posicionamento, ICP, tom de voz e DNA da marca.

**When to Use:** Starting a new project, redefining brand positioning, or onboarding a new client.

**Key Steps:**
1. Problema & Mercado
2. ICP (Ideal Customer Profile)
3. Posicionamento
4. Tom de Voz
5. Promessa & Oferta
6. Narrativa & Storytelling
7. Consolidação

**Agent:** Brand Strategist
**Session:** Multi (Continuable) — can pause and resume
**Type:** Intent-based — collaborative discovery, 1-2 questions per turn

---

### Mandala Builder

**Purpose:** Construir a Mandala da Criatividade Infinita cruzando fases do funil × tipos de criativo.

**When to Use:** After completing the Brand Brief, to generate creative briefs for scaled production.

**Key Steps:**
1. Carregar Brand Brief
2. Definir Fases do Funil
3. Definir Tipos de Criativo
4. Construir Matriz
5. Gerar Briefs
6. Consolidação

**Agent:** VTSD Specialist
**Session:** Multi (Continuable)
**Type:** Intent-based with Prescriptive brief generation
**Depends on:** Brand Brief

---

### Performance Review

**Purpose:** Analisar performance de campanhas a cada 72h e gerar recomendações acionáveis.

**When to Use:** Every 72h during active campaigns (Rapid Test or ongoing).

**Key Steps:**
1. Coleta de Dados
2. Análise de Métricas
3. Identificar Winners
4. Recomendações
5. Relatório

**Agent:** Performance Analyst
**Session:** Single
**Type:** Balanced

---

## Feature Workflows

### Funnel Design

**Purpose:** Projetar o funil completo e a jornada do cliente com todos os touchpoints.

**When to Use:** When designing a new funnel or redesigning an existing one.

**Key Steps:** 6 steps — from context to consolidation
**Agent:** Funnel Architect
**Session:** Multi (6 steps)
**Type:** Intent-based
**Depends on:** Brand Brief

---

### Content Plan

**Purpose:** Criar plano editorial estratégico com pilares de conteúdo, calendário e repurpose.

**When to Use:** When establishing content strategy for the project.

**Key Steps:** 5 steps — pillars, formats, calendar, repurpose
**Agent:** Content Strategist
**Session:** Multi (5 steps)
**Type:** Intent-based
**Depends on:** Brand Brief

---

### Ad Batch Generator

**Purpose:** Gerar 20-40 variações de anúncio a partir dos briefs da Mandala.

**When to Use:** After Mandala is complete, to produce ad variations for testing.

**Key Steps:** 4 steps — load briefs, select frameworks, generate, export
**Agent:** Copywriter + Art Director
**Session:** Single
**Type:** Prescriptive
**Depends on:** Mandala Builder

---

### Rapid Test Protocol

**Purpose:** Testar ads com $100 em 3 dias via CPC para identificar winners.

**When to Use:** After generating ad batch, to test which ads perform best.

**Key Steps:** 5 steps — select, configure, track, launch, monitor
**Agent:** Ads Strategist
**Session:** Single
**Type:** Prescriptive
**Depends on:** Ad Batch Generator

---

### Dynamic LP Pipeline

**Purpose:** Gerar LP dedicada por ad winner com deploy automático na VPS.

**When to Use:** After Rapid Test identifies winners, to create matched landing pages.

**Key Steps:** 6 steps — load winners, template, generate, track, deploy, verify
**Agent:** Web Architect + Automation Architect
**Session:** Single
**Type:** Prescriptive
**Depends on:** Rapid Test Protocol
**Requires:** VPS with SSH access

---

### Landing Page Builder

**Purpose:** Construir landing pages individuais completas (standalone, fora do pipeline dinâmico).

**When to Use:** When building individual landing pages for sales, capture, webinars.

**Key Steps:** 5 steps — objective, structure, copy, design, deploy
**Agent:** Web Architect
**Session:** Single
**Type:** Prescriptive

---

### Email Sequence Builder

**Purpose:** Criar sequências completas de email com copy, timing e triggers.

**When to Use:** When building email automation sequences.

**Key Steps:** 5 steps — type, structure, copy, automation, export
**Agent:** Email Copywriter
**Session:** Single
**Type:** Prescriptive

---

### Campaign Builder

**Purpose:** Criar campanhas completas com copy + criativos visuais alinhados.

**When to Use:** For launches, promotions, or structured campaign creation.

**Key Steps:** 6 steps — briefing, concept, copy, visuals, media plan, consolidation
**Agent:** Copywriter + Art Director
**Session:** Single
**Type:** Prescriptive

---

### VSL Structure

**Purpose:** Criar a estrutura completa de um Video Sales Letter com roteiro.

**When to Use:** When creating a VSL from scratch.

**Key Steps:** 6 steps — big idea, problem, story, solution, offer, CTA
**Agent:** VTSD Specialist
**Session:** Single
**Type:** Intent-based

---

### Market Research

**Purpose:** Conduzir pesquisa de mercado com Voice Mining para descobrir as palavras do ICP.

**When to Use:** When needing deep market intelligence and ICP language.

**Key Steps:** 5 steps — scope, sources, voice mining, patterns, report
**Agent:** Market Researcher
**Session:** Multi
**Type:** Balanced
**Requires:** Web Search / Web Fetch tools

---

### Blog Automation Setup

**Purpose:** Configurar pipeline de blog automatizado — da definição de pilares à publicação.

**When to Use:** When setting up automated blog content pipeline.

**Key Steps:** 5 steps — approach, pillars, pipeline setup, test, activate
**Agent:** Automation Architect + Content Strategist
**Session:** Single
**Type:** Balanced

---

## Workflow Chaining (Main Pipeline)

The primary workflow chain follows this sequence:

```
Brand Brief → Mandala Builder → Ad Batch Generator → Rapid Test Protocol
  → Performance Review → Dynamic LP Pipeline → CRO optimization
    → back to VTSD Specialist (new cycle)
```

Each workflow's output becomes the next workflow's input. The chain creates a continuous improvement loop.
