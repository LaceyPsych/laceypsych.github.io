# Lacey Psych

This repository hosts Lacey's public Hugo site for GitHub Pages:

```text
https://lacey.life/
https://laceypsych.github.io/
```

The site publishes psychology and therapy-adjacent essays, starting with the
Human Architecture Theory series. Posts are educational reflections, not
diagnosis, therapy, or treatment.

The editorial issue tracker lives in this repository. The highest priority
issues are Lacey-authored drafts and knowledge-map items already opened here;
migrated outreach backlog items follow those in the weekly cadence.

## Publishing

The site is built with Hugo and deployed by GitHub Actions.

- Pull requests run `hugo --minify` as a build check.
- Merges to `main` upload the built site to GitHub Pages.
- `CNAME` configures the custom domain `lacey.life`.
- Generated `public/` output is not committed.

## Operating Docs

- [Editorial strategy](docs/editorial-strategy.md)
- [Publishing workflow](docs/publishing-workflow.md)
- [Lacey Pages setup runbook](docs/lacey-pages-setup.md)
- [Content roadmap](docs/content-roadmap.md)
- [Provenance map](docs/provenance-map.md)
- [Draft template](docs/draft-template.md)

## Repos Used As Source Material

- `/Users/ranjib/workspace/PsychSimulator`: simulator contracts, reference
  engines, psychological dials, profile examples, reproducibility/governance
  rules.
- `/Users/ranjib/workspace/Psych-LLM-Wiki`: concept graph, instrument graph,
  reviewed source cards, book chapters, and source-backed claims.

## Workflow

1. Open a GitHub issue for each post idea using the blog post issue template.
2. Prioritize existing Lacey-authored issues before migrated outreach backlog.
3. Build the outline from the content roadmap and provenance map.
4. Lacey reviews voice, clinical framing, and academic caution.
5. Publish one longform post per week through a pull request.
6. Create LinkedIn, Instagram, and Facebook variants from the same source post.

## Site Layout

- `content/posts/`: public essays.
- `content/about.md`: public About page.
- `assets/css/site.css`: site styling.
- `layouts/`: Hugo templates.
- `.github/workflows/pages.yml`: Pages build and deploy workflow.
