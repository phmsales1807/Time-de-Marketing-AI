# Workflow Specification: Brand Brief

**Module:** mmad
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-23

---

## Workflow Overview

**Goal:** Facilitar a descoberta do posicionamento, ICP, tom de voz e DNA da marca através de uma conversa guiada.

**Description:** Workflow colaborativo e intent-based que guia o usuário através de 7 steps para construir o documento-mãe do projeto — o Brand Brief. Ele não gera respostas; facilita a descoberta do posicionamento único de cada negócio. O output alimenta todos os outros workflows do MMAD.

**Workflow Type:** Intent-based (Collaborative)

---

## Workflow Structure

### Entry Point

```yaml
---
name: brand-brief
description: Facilita a descoberta do posicionamento, ICP, tom de voz e DNA da marca
web_bundle: true
installed_path: '{project-root}/_bmad/mmad/workflows/brand-brief'
---
```

### Mode

- [x] Create-only (steps-c/)
- [ ] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Problema & Mercado | Identificar o problema central que o produto resolve e o mercado-alvo |
| 2 | ICP (Ideal Customer Profile) | Definir o perfil do cliente ideal com profundidade |
| 3 | Posicionamento | Descobrir o posicionamento único e diferenciadores |
| 4 | Tom de Voz | Estabelecer a personalidade da comunicação da marca |
| 5 | Promessa & Oferta | Articular a promessa central e estrutura da oferta |
| 6 | Narrativa & Storytelling | Construir a narrativa fundacional da marca |
| 7 | Consolidação | Compilar o Brand Brief final com todos os elementos |

---

## Workflow Inputs

### Required Inputs

- Conhecimento do usuário sobre seu próprio negócio/produto
- Disposição para responder perguntas estratégicas (1-2 por turno)

### Optional Inputs

- Materiais existentes de marca (se houver)
- Pesquisas de mercado anteriores
- Dados de clientes existentes

---

## Workflow Outputs

### Output Format

- [x] Document-producing
- [ ] Non-document

### Output Files

- `brand-brief-{project}.md` — Documento completo do Brand Brief com todas as seções

---

## Agent Integration

### Primary Agent

Brand Strategist — Arquiteto de marca, facilita descoberta com tom consultivo

### Other Agents

Nenhum — Este é o workflow fundacional que alimenta os demais

---

## Implementation Notes

**Use the create-workflow workflow to build this workflow.**

Notas importantes:
- Session type: Multi (Continuable) — o usuário pode pausar e retomar
- O agente deve perguntar 1-2 perguntas por turno, nunca mais
- Facilitation over Generation — o agente guia, não gera
- Este é o documento-mãe: todos os outros workflows dependem dele
- Output em `{document_output_language}` (Brazilian Portuguese)

---

_Spec created on 2026-02-23 via BMAD Module workflow_
