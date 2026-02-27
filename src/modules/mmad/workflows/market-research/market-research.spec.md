# Workflow Specification: Market Research

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Conduzir pesquisa de mercado com Voice Mining para descobrir as palavras exatas do ICP.

**Description:** Workflow balanced que guia o usuário numa pesquisa de mercado aprofundada. Usa Voice Mining (busca em Reddit, comunidades, reviews) para encontrar as palavras, frases e expressões exatas que o ICP usa para descrever suas dores, desejos e objeções.

**Workflow Type:** Balanced (Structured framework + flexible interpretation)

---

## Workflow Structure

### Entry Point

```yaml
---
name: market-research
description: Pesquisa de mercado com Voice Mining para descobrir as palavras do ICP
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/market-research'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Definir Escopo | Definir nicho, ICP e perguntas-chave da pesquisa |
| 2 | Fontes de Dados | Mapear onde o ICP conversa (Reddit, grupos, reviews, fóruns) |
| 3 | Voice Mining | Coletar expressões, frases e palavras exatas do ICP |
| 4 | Análise de Padrões | Identificar padrões recorrentes (dores, desejos, objeções) |
| 5 | Relatório | Compilar relatório com insights e vocabulário do ICP |

---

## Workflow Inputs

### Required Inputs

- Brand Brief (ICP definido)
- Nicho/mercado a pesquisar

### Optional Inputs

- URLs específicas para analisar
- Keywords e termos de busca
- Pesquisas anteriores

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `market-research-{project}.md` — Relatório de pesquisa com Voice Mining, padrões e vocabulário do ICP

---

## Agent Integration

### Primary Agent

Market Researcher — Inteligência de mercado, Voice Mining, tom balanced

### Other Agents

- Brand Strategist — Alinhamento com posicionamento
- Copywriter — Consumirá o vocabulário do ICP para copy

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Multi
- Speed Protocol: Voice Mining
- Requer: Web Search / Web Fetch MCP tools
- As palavras exatas do ICP são ouro para copy e ads
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
