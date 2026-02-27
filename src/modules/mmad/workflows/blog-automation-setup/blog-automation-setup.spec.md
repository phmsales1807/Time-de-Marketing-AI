# Workflow Specification: Blog Automation Setup

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Configurar pipeline de blog automatizado — da definição de pilares à publicação automática.

**Description:** Workflow balanced que configura o pipeline de conteúdo SEO automatizado. Duas opções: (A) Automarticles (recomendada) para produção e publicação automatizada, ou (B) pipeline custom com Content Strategist + Copywriter + Automation Architect via WordPress/Ghost REST API.

**Workflow Type:** Balanced (Structured setup + flexible choice)

---

## Workflow Structure

### Entry Point

```yaml
---
name: blog-automation-setup
description: Setup de blog automatizado com Automarticles ou pipeline custom
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/blog-automation-setup'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Escolher Abordagem | Selecionar Automarticles (A) ou Custom Pipeline (B) |
| 2 | Definir Pilares SEO | Definir pilares de conteúdo para SEO |
| 3 | Configurar Pipeline | Setup da ferramenta escolhida |
| 4 | Teste & Validação | Publicar post de teste e validar pipeline |
| 5 | Ativação | Ativar pipeline com calendário de publicação |

---

## Workflow Inputs

### Required Inputs

- Content Plan (pilares editoriais definidos)
- Plataforma de blog (WordPress, Ghost)
- Acesso à plataforma (API keys ou credenciais)

### Optional Inputs

- Keywords SEO já pesquisadas
- Posts existentes (para manter consistência)
- Frequência de publicação desejada

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `blog-automation-{project}.md` — Configuração completa do pipeline com setup, calendário e regras

---

## Agent Integration

### Primary Agent

Automation Architect — DevOps do marketing, setup de integrações

### Other Agents

- Content Strategist — Pilares e estratégia de conteúdo
- Copywriter — Template de posts (se pipeline custom)

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Automation Pipeline: Blog Automation (Medium Priority)
- Opção A (Automarticles) é recomendada por simplicidade
- Opção B requer WordPress/Ghost REST API na VPS
- Automation Architect tem sidecar para manter configs entre sessões
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
