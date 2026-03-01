# TODO: MMAD - Marketing Method of Agile AI-Driven Development

Development roadmap for mmad module.

---

## Agents to Build

### Layer 1 — Strategy
- [ ] Brand Strategist (Arquiteto de marca)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/brand-strategist/brand-strategist.spec.md`
- [ ] Market Researcher (Inteligência de mercado)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/market-researcher/market-researcher.spec.md`
- [ ] Funnel Architect (Designer de jornada)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/funnel-architect/funnel-architect.spec.md`

### Layer 2 — Sales Engine
- [ ] VTSD Specialist (Cérebro comercial)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/vtsd-specialist/vtsd-specialist.spec.md`
  - Note: Has sidecar for persistent memory

### Layer 3 — Foundation
- [ ] Brand Designer (Identidade visual)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/brand-designer/brand-designer.spec.md`
- [ ] Web Architect (Arquitetura web + Dynamic LP)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/web-architect/web-architect.spec.md`
- [ ] Content Strategist (Linha editorial)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/content-strategist/content-strategist.spec.md`

### Layer 4 — Production
- [ ] Copywriter (Textos persuasivos)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/copywriter/copywriter.spec.md`
- [x] ~~Art Director~~ → Absorbed into Brand Designer (Laura)
- [ ] Video Producer (Conteúdo audiovisual)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/video-producer/video-producer.spec.md`
- [x] ~~Email Copywriter~~ → Absorbed into Copywriter (Nanda)

### Layer 4.5 — Platforms
- [ ] YouTube Specialist (Ecossistema YouTube)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/youtube-specialist/youtube-specialist.spec.md`
- [ ] Instagram Specialist (Superfícies IG)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/instagram-specialist/instagram-specialist.spec.md`
- [ ] TikTok Specialist (Nativo TikTok)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/tiktok-specialist/tiktok-specialist.spec.md`

### Layer 5 — Distribution
- [ ] Acquisition Strategist (Campanhas pagas + Growth)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/ads-strategist/ads-strategist.spec.md`
- [x] ~~Social Media Manager~~ → Absorbed into Content Strategist (Ana)
- [x] ~~Growth Hacker~~ → Absorbed into Acquisition Strategist (Tiago)
- [x] ~~Lead Activation Specialist~~ → Absorbed into Funnel Architect (Davi)

### Layer 6 — Analysis
- [ ] Performance Analyst (Dados e insights)
  - Use: `bmad:bmb:agents:agent-builder`
  - Spec: `agents/performance-analyst/performance-analyst.spec.md`
  - Note: Has sidecar for persistent memory
- [x] ~~CRO Specialist~~ → Absorbed into Performance Analyst (Gabi)
- [x] ~~Creative Reviewer~~ → Absorbed into Brand Designer (Laura)
- [x] ~~Automation Architect~~ → Absorbed into Web Architect (João)

---

## Workflows to Build

### Core Workflows
- [ ] Brand Brief
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/brand-brief/brand-brief.spec.md`
- [ ] Mandala Builder
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/mandala-builder/mandala-builder.spec.md`
- [ ] Performance Review
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/performance-review/performance-review.spec.md`

### Feature Workflows
- [ ] Funnel Design
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/funnel-design/funnel-design.spec.md`
- [ ] Content Plan
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/content-plan/content-plan.spec.md`
- [ ] Ad Batch Generator
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/ad-batch-generator/ad-batch-generator.spec.md`
- [ ] Rapid Test Protocol
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/rapid-test-protocol/rapid-test-protocol.spec.md`
- [ ] Dynamic LP Pipeline
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/dynamic-lp-pipeline/dynamic-lp-pipeline.spec.md`
- [ ] Landing Page Builder
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/landing-page-builder/landing-page-builder.spec.md`
- [ ] Email Sequence Builder
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/email-sequence-builder/email-sequence-builder.spec.md`
- [ ] Campaign Builder
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/campaign-builder/campaign-builder.spec.md`
- [ ] VSL Structure
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/vsl-structure/vsl-structure.spec.md`
- [ ] Market Research
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/market-research/market-research.spec.md`
- [ ] Blog Automation Setup
  - Use: `bmad:bmb:workflows:workflow` or `/workflow`
  - Spec: `workflows/blog-automation-setup/blog-automation-setup.spec.md`

---

## Installation Testing

- [ ] Test installation with `bmad install`
- [ ] Verify module.yaml prompts work correctly
- [ ] Verify all agents and workflows are discoverable

---

## Documentation

- [ ] Complete README.md with usage examples
- [ ] Enhance docs/ folder with more guides
- [ ] Add troubleshooting section
- [ ] Document configuration options

---

## Recommended Build Order

Follow the Implementation Roadmap from the brief:

| Sprint | Focus | Components |
|--------|-------|------------|
| 1 | Brand Strategist agent + Brand Brief workflow | Test isolated |
| 2 | VTSD Specialist agent + Mandala Builder workflow | Test isolated |
| 3 | Chain: Brand Brief → Mandala Builder | Test handoff |
| 4 | Copywriter agent + Ad Batch Generator | Test batch |
| 5 | Ads Strategist + Rapid Test Protocol | Test protocol |
| 6 | Performance Analyst + 72h Review | Test feedback loop |
| 7 | Web Architect + Dynamic LP Pipeline | Test pipeline |
| 8 | Automation Architect + Deploy VPS setup | Test deploy |
| 9 | Full chain: Mandala → Batch → Test → LP → Review | Test loop |
| 10 | Blog Automation Setup | Test automation |

---

## Next Steps

1. Build agents using create-agent workflow
2. Build workflows using create-workflow workflow
3. Test installation and functionality
4. Iterate based on testing (3-5 iterations per workflow)

---

_Last updated: 2026-02-23_
