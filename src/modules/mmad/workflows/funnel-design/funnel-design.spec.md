# Workflow Specification: Funnel Design

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Projetar o funil completo e a jornada do cliente com todos os touchpoints.

**Description:** Workflow intent-based que guia o usuário no design do funil de vendas completo — da aquisição à conversão e retenção. Mapeia todos os touchpoints, canais e momentos de decisão do cliente.

**Workflow Type:** Intent-based (Collaborative)

---

## Workflow Structure

### Entry Point

```yaml
---
name: funnel-design
description: Design de funil e jornada do cliente com todos os touchpoints
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/funnel-design'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Contexto & Objetivo | Definir o objetivo do funil e carregar Brand Brief |
| 2 | Mapeamento de Fases | Definir as fases do funil (topo, meio, fundo) |
| 3 | Touchpoints & Canais | Mapear pontos de contato e canais por fase |
| 4 | Conteúdo por Fase | Definir tipo de conteúdo/oferta para cada touchpoint |
| 5 | Métricas & KPIs | Estabelecer métricas de sucesso por fase |
| 6 | Consolidação | Compilar o design completo do funil |

---

## Workflow Inputs

### Required Inputs

- Brand Brief completo
- Produto/oferta definidos

### Optional Inputs

- Funil existente (para redesign)
- Dados de conversão atuais

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `funnel-design-{project}.md` — Design completo do funil com todas as fases, touchpoints e métricas

---

## Agent Integration

### Primary Agent

Funnel Architect — Designer de jornada do cliente, tom consultivo

### Other Agents

- Brand Strategist (referência ao Brand Brief)
- Content Strategist (alinhamento de conteúdo por fase)

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Multi (6 steps)
- Depende do Brand Brief (workflow chaining)
- Intent-based: facilita descoberta da jornada ideal
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
