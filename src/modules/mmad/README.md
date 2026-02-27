# MMAD: Marketing Method of Agile AI-Driven Development

Framework completo de marketing digital com agentes especializados, workflows guiados e protocolos de automação

22 agentes | 14 workflows | 7 camadas | Da estratégia à execução com feedback loops contínuos

---

## Overview

O MMAD organiza todo o ecossistema de marketing digital em agentes de IA especializados, workflows estruturados e protocolos de automação. Inspirado no BMAD Method para desenvolvimento de software, o MMAD adapta o conceito de "Agentic Agile" para marketing — da estratégia à execução, com feedback loops contínuos.

O módulo opera em 7 camadas com abordagem mix:
- **Estratégicos** (Camadas 1-2): Intent-based — facilitam descoberta
- **Operacionais** (Camadas 3-5): Prescriptive — executam com consistência em escala
- **Analíticos** (Camada 6): Balanced — framework fixo, interpretação flexível
- **Automação** (Camada 7): Balanced — integrações e deploy

---

## Installation

```bash
bmad install mmad
```

---

## Quick Start

1. Start with the **Brand Strategist** agent to create your Brand Brief
2. Use the **VTSD Specialist** to build your Mandala da Criatividade Infinita
3. Generate 20-40 ad variations with the **Copywriter** via Ad Batch Generator
4. Test with $100/3 days using the **Ads Strategist** Rapid Test Protocol
5. Deploy Dynamic LPs for winners with the **Web Architect**
6. Review performance every 72h with the **Performance Analyst**

**For detailed documentation, see [docs/](docs/).**

---

## Components

### Agents

| # | Agent | Layer | Role |
|---|-------|-------|------|
| 1 | Brand Strategist | 1 - Strategy | Arquiteto de marca. Define o DNA do projeto |
| 2 | Market Researcher | 1 - Strategy | Inteligência de mercado. Voice Mining |
| 3 | Funnel Architect | 1 - Strategy | Designer de jornada do cliente |
| 4 | VTSD Specialist | 2 - Sales Engine | Cérebro comercial. Mandala, Perpétuo, Light Copy |
| 5 | Brand Designer | 3 - Foundation | Identidade visual completa |
| 6 | Web Architect | 3 - Foundation | Arquitetura web + Dynamic LP Pipeline |
| 7 | Content Strategist | 3 - Foundation | Linha editorial, pilares, calendário macro |
| 8 | Copywriter | 4 - Production | Textos persuasivos. Batch generation |
| 9 | Art Director | 4 - Production | Criativos visuais. Batch com React → PNG |
| 10 | Video Producer | 4 - Production | Conteúdo audiovisual. AI UGC first |
| 11 | Email Copywriter | 4 - Production | Sequências de email e mensageria |
| 12 | YouTube Specialist | 4.5 - Platforms | Ecossistema YouTube completo |
| 13 | Instagram Specialist | 4.5 - Platforms | Todas as superfícies IG |
| 14 | TikTok Specialist | 4.5 - Platforms | Nativo TikTok |
| 15 | Ads Strategist | 5 - Distribution | Campanhas pagas. Rapid Test Protocol |
| 16 | Social Media Manager | 5 - Distribution | Presença orgânica |
| 17 | Growth Hacker | 5 - Distribution | Aquisição e crescimento acelerado |
| 18 | Lead Activation Specialist | 5 - Distribution | Ativação de leads, cadências multicanal |
| 19 | Performance Analyst | 6 - Analysis | Dados, insights, 72h feedback loop |
| 20 | CRO Specialist | 6 - Analysis | Otimização de conversão |
| 21 | Creative Reviewer | 6 - Analysis | QA de marca |
| 22 | Automation Architect | 7 - Automation | DevOps do marketing. Stack, APIs, deploy |

### Workflows

**Core Workflows:**
| Workflow | Agent | Type | Description |
|----------|-------|------|-------------|
| Brand Brief | Brand Strategist | Intent-based | Brand discovery em 7 steps colaborativos |
| Mandala Builder | VTSD Specialist | Intent-based | Mandala da Criatividade Infinita |
| Performance Review | Performance Analyst | Balanced | Análise de performance a cada 72h |

**Feature Workflows:**
| Workflow | Agent | Type | Description |
|----------|-------|------|-------------|
| Funnel Design | Funnel Architect | Intent-based | Design de funil e jornada do cliente |
| Content Plan | Content Strategist | Intent-based | Plano editorial estratégico |
| Ad Batch Generator | Copywriter + Art Director | Prescriptive | 20-40 variações de ad em batch |
| Rapid Test Protocol | Ads Strategist | Prescriptive | $100/3 dias em CPC → winners |
| Dynamic LP Pipeline | Web Architect + Automation | Prescriptive | LP dedicada por winner → deploy VPS |
| Landing Page Builder | Web Architect | Prescriptive | LPs individuais |
| Email Sequence Builder | Email Copywriter | Prescriptive | Sequências completas de email |
| Campaign Builder | Copywriter + Art Director | Prescriptive | Campanhas completas |
| VSL Structure | VTSD Specialist | Intent-based | Video Sales Letter |
| Market Research | Market Researcher | Balanced | Voice Mining |
| Blog Automation Setup | Automation + Content | Balanced | Pipeline de blog automatizado |

---

## Configuration

The module supports these configuration options (set during installation):

| Config Key | Description | Default |
|------------|-------------|---------|
| `project_name` | Name of your project or brand | Directory name |
| `project_type` | Type of project (infoproduto, ecommerce, saas, negocio-local, agencia) | infoproduto |
| `platforms` | Priority social media platforms | instagram, youtube, tiktok |
| `mmad_output` | Output folder for MMAD files | `{output_folder}/mmad` |
| `brand_assets` | Brand assets folder | `{output_folder}/mmad/brand` |
| `campaign_assets` | Campaign assets folder | `{output_folder}/mmad/campaigns` |
| `content_assets` | Content assets folder | `{output_folder}/mmad/content` |
| `funnel_assets` | Funnel assets folder | `{output_folder}/mmad/funnels` |
| `analytics_assets` | Analytics reports folder | `{output_folder}/mmad/analytics` |
| `vps_deploy_enabled` | VPS available for Dynamic LP Pipeline | false |

---

## Module Structure

```
mmad/
├── module.yaml
├── README.md
├── TODO.md
├── docs/
│   ├── getting-started.md
│   ├── agents.md
│   ├── workflows.md
│   └── examples.md
├── agents/
│   ├── brand-strategist/
│   ├── market-researcher/
│   ├── funnel-architect/
│   ├── vtsd-specialist/
│   ├── brand-designer/
│   ├── web-architect/
│   ├── content-strategist/
│   ├── copywriter/
│   ├── art-director/
│   ├── video-producer/
│   ├── email-copywriter/
│   ├── youtube-specialist/
│   ├── instagram-specialist/
│   ├── tiktok-specialist/
│   ├── ads-strategist/
│   ├── social-media-manager/
│   ├── growth-hacker/
│   ├── lead-activation-specialist/
│   ├── performance-analyst/
│   ├── cro-specialist/
│   ├── creative-reviewer/
│   └── automation-architect/
├── workflows/
│   ├── brand-brief/
│   ├── mandala-builder/
│   ├── performance-review/
│   ├── funnel-design/
│   ├── content-plan/
│   ├── ad-batch-generator/
│   ├── rapid-test-protocol/
│   ├── dynamic-lp-pipeline/
│   ├── landing-page-builder/
│   ├── email-sequence-builder/
│   ├── campaign-builder/
│   ├── vsl-structure/
│   ├── market-research/
│   └── blog-automation-setup/
└── data/
    ├── mandala-matrix.md
    ├── copy-frameworks.md
    └── platform-specs.md
```

---

## Documentation

For detailed user guides and documentation, see the **[docs/](docs/)** folder:
- [Getting Started](docs/getting-started.md)
- [Agents Reference](docs/agents.md)
- [Workflows Reference](docs/workflows.md)
- [Examples](docs/examples.md)

---

## Development Status

This module is currently in development. The following components are planned:

- [ ] Agents: 22 agents
- [ ] Workflows: 14 workflows

See TODO.md for detailed status.

---

## Author

Created by Babi via BMAD Module workflow

---

## License

Part of the BMAD framework.
