# Workflow Specification: Mandala Builder

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Construir a Mandala da Criatividade Infinita: cruzar fases do funil × tipos de criativo para gerar briefs de produção em escala.

**Description:** Workflow intent-based que constrói a Mandala — uma matriz criativa que cruza fases do funil de vendas com tipos de criativo. O resultado são briefs estruturados para produção em batch. Utiliza o método VTSD (Mandala da Criatividade Infinita) como framework.

**Workflow Type:** Intent-based (Collaborative) com elementos Prescriptive na geração de briefs

---

## Workflow Structure

### Entry Point

```yaml
---
name: mandala-builder
description: Constrói a Mandala da Criatividade Infinita cruzando funil × criativos
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/mandala-builder'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Carregar Brand Brief | Validar que o Brand Brief existe e carregar contexto |
| 2 | Definir Fases do Funil | Mapear as fases do funil relevantes para o produto |
| 3 | Definir Tipos de Criativo | Selecionar os formatos de criativo disponíveis |
| 4 | Construir Matriz | Cruzar funil × criativos gerando a Mandala |
| 5 | Gerar Briefs | Criar briefs de produção para cada célula priorizada |
| 6 | Consolidação | Compilar a Mandala final com briefs priorizados |

---

## Workflow Inputs

### Required Inputs

- Brand Brief completo (`brand-brief-{project}.md`)
- Conhecimento do usuário sobre fases do funil do seu produto

### Optional Inputs

- Histórico de campanhas anteriores (via sidecar do VTSD Specialist)
- Premissas já testadas
- Dados de performance de campanhas passadas

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `mandala-{project}.md` — Mandala completa com matriz e briefs priorizados
- `batch-briefs-{project}.md` — Briefs individuais para produção em batch

---

## Agent Integration

### Primary Agent

VTSD Specialist — Cérebro comercial, método VTSD, Mandala, Perpétuo, Light Copy

### Other Agents

- Brand Strategist (referência ao Brand Brief)
- Copywriter (consumirá os briefs gerados)
- Art Director (consumirá os briefs gerados)

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Multi (Continuable)
- Depende do Brand Brief (workflow chaining)
- O VTSD Specialist tem sidecar — pode consultar histórico entre sessões
- Reference: `data/mandala-matrix.md` para framework da Mandala
- "A Mandala decidiu" — catchphrase ao recomendar ângulos
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
