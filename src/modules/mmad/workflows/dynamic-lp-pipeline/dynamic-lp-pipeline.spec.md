# Workflow Specification: Dynamic LP Pipeline

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Gerar landing page dedicada por ad winner com a mesma headline, deploy automático na VPS, zero dissonância cognitiva.

**Description:** Workflow prescriptive que pega cada ad vencedor do Rapid Test e gera uma landing page dedicada. A headline do ad = headline da LP. Template base reutilizável, customizado por ângulo. Deploy automático via SSH/rsync na VPS do usuário. Tracking individual por LP.

**Workflow Type:** Prescriptive (Pipeline-driven)

---

## Workflow Structure

### Entry Point

```yaml
---
name: dynamic-lp-pipeline
description: Gera LP dedicada por ad winner → deploy automático na VPS
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/dynamic-lp-pipeline'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Carregar Winners | Identificar ads winners do Rapid Test |
| 2 | Template Base | Selecionar/configurar template base da LP |
| 3 | Gerar LPs | Criar LP customizada por winner (headline, copy, CTA) |
| 4 | Configurar Tracking | Pixel, UTMs e tracking individual por LP |
| 5 | Deploy VPS | Deploy automático via SSH/rsync/git na VPS |
| 6 | Verificação | Confirmar URLs ativas e tracking funcionando |

---

## Workflow Inputs

### Required Inputs

- Resultado do Rapid Test com winners identificados
- Acesso SSH à VPS (configurado previamente)
- Template base de LP (HTML)

### Optional Inputs

- Brand guidelines para design da LP
- Domínio/subdomínio para as LPs
- Configuração de CDN/SSL

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `dynamic-lp-{date}-{project}.md` — Relatório de deploy com URLs, tracking IDs e status
- Arquivos HTML das LPs (deployados na VPS)

---

## Agent Integration

### Primary Agent

Web Architect — Arquitetura web, Dynamic LP Pipeline, "Zero dissonância"

### Other Agents

- Automation Architect — Deploy VPS, SSH/rsync, configuração de servidor
- Copywriter — Copy da LP alinhada ao ad winner
- Performance Analyst — Tracking e análise pós-deploy

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Single
- Automation Pipeline: Dynamic LP Pipeline (High Priority)
- Princípios: Headline do ad = Headline da LP | 1 LP por ângulo | Template base reutilizável
- Deploy em segundos, não dias
- "Zero dissonância" — catchphrase do Web Architect
- Depende de: Rapid Test Protocol (workflow chaining)
- Alimenta: Performance Review (72h depois)
- Requer: Bash/SSH tools para deploy
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
