# Workflow Specification: VSL Structure

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Criar a estrutura completa de um Video Sales Letter (VSL) com roteiro e storytelling.

**Description:** Workflow intent-based que guia o usuário na construção de um VSL completo — desde a big idea até o fechamento com CTA. Usa frameworks de persuasão e storytelling para criar um roteiro que converte.

**Workflow Type:** Intent-based (Collaborative)

---

## Workflow Structure

### Entry Point

```yaml
---
name: vsl-structure
description: Estrutura completa de Video Sales Letter com roteiro e storytelling
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/vsl-structure'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Big Idea & Hook | Definir a ideia central e o gancho de abertura |
| 2 | Problema & Agitação | Aprofundar na dor do ICP e amplificar urgência |
| 3 | História & Credibilidade | Construir narrativa de autoridade e prova |
| 4 | Solução & Mecanismo | Apresentar a solução e o mecanismo único |
| 5 | Oferta & Stack | Estruturar a oferta com stack de valor |
| 6 | Fechamento & CTA | Criar fechamento persuasivo com urgência e CTA |

---

## Workflow Inputs

### Required Inputs

- Brand Brief completo
- Produto/oferta definidos
- ICP com dores mapeadas

### Optional Inputs

- Mandala (ângulo específico para o VSL)
- Depoimentos/provas sociais disponíveis
- Dados de conversão de VSLs anteriores

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `vsl-{name}-{project}.md` — Roteiro completo do VSL com todas as seções e indicações de timing

---

## Agent Integration

### Primary Agent

VTSD Specialist — Estrategista de vendas, método VTSD, Light Copy

### Other Agents

- Copywriter — Refinamento de copy específica
- Video Producer — Indicações de produção audiovisual

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Intent-based: facilita descoberta da big idea e narrativa
- Reference: `data/copy-frameworks.md` para frameworks de persuasão
- Método VTSD integrado
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
