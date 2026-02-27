# Workflow Specification: Ad Batch Generator

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Gerar 20-40 variações de anúncio a partir dos briefs da Mandala em uma única sessão.

**Description:** Workflow prescriptive que recebe os briefs da Mandala e gera variações de ads em batch. Cada variação segue os frameworks de copy definidos (`data/copy-frameworks.md`) e inclui headline, body e CTA. O mercado decide o vencedor via Rapid Test.

**Workflow Type:** Prescriptive (Framework-driven, consistent at scale)

---

## Workflow Structure

### Entry Point

```yaml
---
name: ad-batch-generator
description: Gera 20-40 variações de ad a partir dos briefs da Mandala
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/ad-batch-generator'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Carregar Briefs | Validar e carregar briefs da Mandala |
| 2 | Selecionar Frameworks | Escolher frameworks de copy para cada ângulo |
| 3 | Gerar Variações | Produzir 20-40 variações (headline + body + CTA) |
| 4 | Revisão & Export | Revisar batch e exportar para formato de campanha |

---

## Workflow Inputs

### Required Inputs

- Mandala completa com briefs priorizados (`mandala-{project}.md`)
- Brand Brief (referência de tom de voz)

### Optional Inputs

- Copy frameworks preferidos
- Restrições de plataforma (limite de caracteres)
- Exemplos de ads anteriores que performaram bem

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `ad-batch-{date}-{project}.md` — Batch completo com 20-40 variações de ad

---

## Agent Integration

### Primary Agent

Copywriter — Textos persuasivos, batch generation, tom executivo e direto

### Other Agents

- Art Director — Criativos visuais correspondentes (React → PNG)
- VTSD Specialist — Referência aos briefs da Mandala

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Prescriptive: segue frameworks de copy com consistência
- Reference: `data/copy-frameworks.md` para frameworks de persuasão
- Depende da Mandala (workflow chaining)
- Speed Protocol: Batch Generation
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
