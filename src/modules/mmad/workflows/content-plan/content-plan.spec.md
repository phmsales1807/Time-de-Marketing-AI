# Workflow Specification: Content Plan

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Criar plano editorial estratégico com pilares de conteúdo, calendário macro e estratégia de repurpose.

**Description:** Workflow intent-based que guia o usuário na criação de uma estratégia de conteúdo completa. Define pilares editoriais alinhados à marca, calendário de publicação e estratégia de reaproveitamento de conteúdo entre plataformas.

**Workflow Type:** Intent-based (Collaborative)

---

## Workflow Structure

### Entry Point

```yaml
---
name: content-plan
description: Plano editorial estratégico com pilares, calendário e repurpose
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/content-plan'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Contexto & Brand Brief | Carregar contexto da marca e definir objetivos de conteúdo |
| 2 | Pilares Editoriais | Definir 3-5 pilares de conteúdo alinhados à marca |
| 3 | Formatos & Plataformas | Mapear formatos por plataforma (IG, YT, TikTok, Blog) |
| 4 | Calendário Macro | Criar calendário mensal com distribuição por pilar |
| 5 | Estratégia de Repurpose | Definir como reaproveitar conteúdo entre plataformas |

---

## Workflow Inputs

### Required Inputs

- Brand Brief completo
- Plataformas prioritárias (definidas na config do módulo)

### Optional Inputs

- Conteúdos existentes
- Dados de engajamento de conteúdos anteriores
- Calendário de eventos/lançamentos

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `content-plan-{project}.md` — Plano editorial completo com pilares, calendário e estratégia de repurpose

---

## Agent Integration

### Primary Agent

Content Strategist — Linha editorial, pilares, calendário macro

### Other Agents

- Brand Strategist (referência ao Brand Brief e tom de voz)
- YouTube Specialist, Instagram Specialist, TikTok Specialist (especificidades por plataforma)

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Multi (5 steps)
- Depende do Brand Brief (workflow chaining)
- Reference: `data/platform-specs.md` para especificidades de cada plataforma
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
