# Workflow Specification: Campaign Builder

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Criar campanhas completas com copy + criativos visuais alinhados.

**Description:** Workflow prescriptive que gera campanhas de marketing completas — combinando copy persuasiva com criativos visuais. Diferente do Ad Batch Generator (foco em variações de teste), o Campaign Builder cria campanhas estruturadas para lançamentos, promoções ou picos de vendas.

**Workflow Type:** Prescriptive (Framework-driven)

---

## Workflow Structure

### Entry Point

```yaml
---
name: campaign-builder
description: Campanhas completas com copy + criativos visuais alinhados
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/campaign-builder'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Briefing da Campanha | Definir objetivo, público, oferta e prazo |
| 2 | Conceito Criativo | Definir conceito central e ângulo da campanha |
| 3 | Copy | Gerar copy para cada peça (ads, emails, LPs, social) |
| 4 | Criativos Visuais | Gerar direção de arte para cada peça |
| 5 | Plano de Mídia | Definir distribuição, budget e cronograma |
| 6 | Consolidação | Compilar campanha completa com todos os assets |

---

## Workflow Inputs

### Required Inputs

- Brand Brief (identidade e tom de voz)
- Objetivo da campanha (lançamento, promoção, perpétuo)
- Oferta/produto

### Optional Inputs

- Mandala (ângulos disponíveis)
- Budget disponível
- Datas-chave (lançamento, Black Friday, etc.)

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `campaign-{name}-{project}.md` — Campanha completa com copy, direção de arte, plano de mídia

---

## Agent Integration

### Primary Agent

Copywriter — Copy persuasiva para todas as peças

### Other Agents

- Art Director — Criativos visuais (React → PNG)
- Ads Strategist — Estrutura de campanha paga
- Email Copywriter — Sequências de email da campanha

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Diferente do Ad Batch Generator (este é campanha completa, não batch de teste)
- Pode incluir Picos de Vendas (método VTSD)
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
