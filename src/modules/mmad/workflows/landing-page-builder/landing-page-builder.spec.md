# Workflow Specification: Landing Page Builder

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Construir landing pages individuais completas, fora do pipeline dinâmico.

**Description:** Workflow prescriptive para construção de landing pages standalone. Diferente do Dynamic LP Pipeline (que é automatizado para ads winners), este workflow foca em LPs individuais com mais personalização — páginas de vendas, captura, webinar, etc.

**Workflow Type:** Prescriptive (Template-driven)

---

## Workflow Structure

### Entry Point

```yaml
---
name: landing-page-builder
description: Construção de landing pages individuais completas
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/landing-page-builder'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Objetivo & Tipo | Definir objetivo da LP (vendas, captura, webinar) e tipo |
| 2 | Estrutura & Seções | Definir seções da LP (hero, benefícios, prova social, CTA) |
| 3 | Copy | Escrever copy para cada seção |
| 4 | Design & Build | Gerar HTML/CSS da LP |
| 5 | Deploy | Deploy na VPS ou plataforma escolhida |

---

## Workflow Inputs

### Required Inputs

- Brand Brief (tom de voz e identidade)
- Objetivo da LP e oferta

### Optional Inputs

- Template preferido
- Referências visuais
- Dados de conversão de LPs anteriores

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `lp-{name}-{project}.md` — Spec da LP com copy e estrutura
- Arquivos HTML/CSS da LP

---

## Agent Integration

### Primary Agent

Web Architect — Arquitetura web, construção de LPs

### Other Agents

- Copywriter — Copy persuasiva para as seções
- Brand Designer — Alinhamento visual com identidade da marca

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Diferente do Dynamic LP Pipeline (este é manual/individual)
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
