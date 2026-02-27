# Workflow Specification: Performance Review

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Analisar performance de campanhas a cada 72h, identificar winners e gerar recomendações acionáveis.

**Description:** Workflow balanced que coleta dados de campanhas ativas, analisa métricas-chave (CPC, CTR, CPA, ROAS), identifica ads vencedores e perdedores, e gera recomendações claras: escalar, pausar ou iterar. Framework de coleta fixo, interpretação flexível.

**Workflow Type:** Balanced (Structured collection + flexible interpretation)

---

## Workflow Structure

### Entry Point

```yaml
---
name: performance-review
description: Análise de performance a cada 72h com recomendações acionáveis
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/performance-review'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Coleta de Dados | Reunir métricas das campanhas ativas (manual ou API) |
| 2 | Análise de Métricas | Avaliar CPC, CTR, CPA, ROAS por ad/ângulo |
| 3 | Identificar Winners | Classificar ads em winners, potenciais e perdedores |
| 4 | Recomendações | Gerar decisões: escalar, pausar, iterar |
| 5 | Relatório | Compilar relatório com insights e próximos passos |

---

## Workflow Inputs

### Required Inputs

- Dados de performance das campanhas ativas (métricas: impressões, cliques, CPC, CTR, conversões, CPA, ROAS)
- Período de análise (padrão: últimas 72h)

### Optional Inputs

- Histórico de reviews anteriores (via sidecar do Performance Analyst)
- Metas de CPA/ROAS definidas
- Budget total disponível

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `review-{date}-{project}.md` — Relatório de performance com winners, insights e recomendações

---

## Agent Integration

### Primary Agent

Performance Analyst — Analista data-driven, tom pragmático, só fala verdade com números

### Other Agents

- Ads Strategist (recebe recomendações de escala/pausa)
- VTSD Specialist (recebe insights para próxima Mandala)
- CRO Specialist (recebe dados para otimização de conversão)

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- O Performance Analyst tem sidecar — armazena histórico de reviews
- 72h countdown — urgência crescente na comunicação
- Feedback loop: output alimenta o próximo ciclo (VTSD → Batch → Test → Review)
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
