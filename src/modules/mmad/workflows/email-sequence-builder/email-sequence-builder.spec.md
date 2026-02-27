# Workflow Specification: Email Sequence Builder

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Criar sequências completas de email: welcome, nurture, sales, cart abandonment.

**Description:** Workflow prescriptive que gera sequências de email completas com copy, timing e triggers. Segue frameworks de email marketing com automação via ActiveCampaign/RD Station.

**Workflow Type:** Prescriptive (Framework-driven)

---

## Workflow Structure

### Entry Point

```yaml
---
name: email-sequence-builder
description: Sequências completas de email com copy, timing e triggers
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/email-sequence-builder'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Tipo de Sequência | Selecionar tipo (welcome, nurture, sales, abandonment) |
| 2 | Estrutura | Definir número de emails, intervalos e triggers |
| 3 | Copy dos Emails | Escrever subject line, preview e body de cada email |
| 4 | Automação | Configurar regras de automação e segmentação |
| 5 | Export | Exportar sequência para implementação na ferramenta |

---

## Workflow Inputs

### Required Inputs

- Brand Brief (tom de voz)
- Tipo de sequência desejada
- Oferta/produto relacionado

### Optional Inputs

- Ferramenta de email (ActiveCampaign, RD Station)
- Segmentos de lista existentes
- Dados de open rate/click rate anteriores

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `email-sequence-{type}-{project}.md` — Sequência completa com copy, timing e regras de automação

---

## Agent Integration

### Primary Agent

Email Copywriter — Sequências de email e mensageria, tom prescriptive

### Other Agents

- Copywriter — Alinhamento de tom e frameworks de copy
- Automation Architect — Integração com ferramentas de automação

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Integração: ActiveCampaign / RD Station APIs
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
