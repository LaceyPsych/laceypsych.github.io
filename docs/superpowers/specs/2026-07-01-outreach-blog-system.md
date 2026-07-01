# Outreach Blog System Spec

Date: 2026-07-01

## Goal

Create a repeatable outreach system that turns PsychSimulator and
Psych-LLM-Wiki concepts into relatable, provenance-backed blog posts for
Lacey's personal brand and eventual PsychSimulator soft launch.

## Inputs

- PsychSimulator reference engines, dials, profile contract, run provenance, and
  governance rules.
- Psych-LLM-Wiki concept graph, source notes, instrument graph, and book.
- Lacey's academic review and personal voice.
- GitHub Pages as the longform publishing channel.
- LinkedIn, Instagram, and Facebook as distribution channels.

## Outputs

- Editorial strategy.
- Publishing workflow.
- Provenance map.
- 12-post initial content roadmap.
- Blog post issue template.
- GitHub issues for the first execution tranche.

## Non-Goals

- Build Lacey's live website in this repo.
- Publish private simulator fixtures.
- Make clinical, diagnostic, or treatment claims.
- Launch the simulator publicly before validation and positioning are ready.

## Architecture

This repo is the editorial control plane:

- GitHub issues track post lifecycle and review tasks.
- Docs define voice, workflow, provenance, and topic sequencing.
- Draft templates standardize longform and social variants.

Lacey's GitHub Pages repo is the publishing plane:

- public posts;
- public assets;
- site config and deployment workflow.

PsychSimulator and Psych-LLM-Wiki are the source planes:

- concepts, dials, and story patterns;
- reviewed source cards and citations;
- governance constraints and provenance discipline.

## Execution Plan

1. Land planning docs in this repo.
2. Create GitHub issues for setup and the first six posts.
3. Draft the first post from the roadmap.
4. Decide Lacey's site generator and Pages repository.
5. Move final Markdown into the Pages repo and publish.
6. Cross-post platform variants and track URLs back on the issue.

## Acceptance Criteria

- A contributor can open one issue and understand the post's hook, concept,
  source spine, review checklist, and social outputs.
- The first 12 topics cover personal life, work life, relationships, decision
  making, coping, emotion regulation, and responsible simulation.
- Every research claim has a source candidate before drafting.
- The workflow keeps unpublished planning separate from public Pages content.
