# Workflow Specification: Rapid Test Protocol

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Testar ads com $100 em 3 dias via CPC para identificar 5 winners de forma rápida e barata.

**Description:** Workflow prescriptive que configura o teste rápido de variações de ads. $100 de budget, 3 dias de teste, otimização por CPC (menor custo-por-clique vence). Identifica 5 winners que avançam para Dynamic LP Pipeline e escala.

**Workflow Type:** Prescriptive (Protocol-driven)

---

## Workflow Structure

### Entry Point

```yaml
---
name: rapid-test-protocol
description: $100 / 3 dias em CPC → identifica winners → decisão em 72h
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/rapid-test-protocol'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Selecionar Ads | Escolher ads do batch para teste (máx 20 por rodada) |
| 2 | Configurar Campanha | Definir estrutura de campanha, budget e segmentação |
| 3 | Setup de Tracking | Configurar pixel, UTMs e tracking por variação |
| 4 | Lançar Teste | Checklist de lançamento e ativação |
| 5 | Monitoramento 72h | Orientações para acompanhamento durante os 3 dias |

---

## Workflow Inputs

### Required Inputs

- Ad batch gerado (`ad-batch-{date}-{project}.md`)
- Plataforma de ads (Meta Ads / Google Ads)
- Budget de teste ($100 padrão)
- Público-alvo / segmentação

### Optional Inputs

- Pixel já configurado
- Campanhas anteriores (referência de CPC médio)
- Preferências de estrutura de campanha (CBO vs ABO)

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `rapid-test-{date}-{project}.md` — Setup completo do teste com estrutura de campanha, tracking e checklist

---

## Agent Integration

### Primary Agent

Ads Strategist — Campanhas pagas, Rapid Test Protocol, tom mix (estratégico + executivo)

### Other Agents

- Performance Analyst — Análise pós-72h (workflow chaining para Performance Review)
- Automation Architect — Setup de tracking/pixel se necessário

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Speed Protocol: Rapid Test
- Encadeia com Performance Review (72h depois)
- Encadeia com Dynamic LP Pipeline (para winners)
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
