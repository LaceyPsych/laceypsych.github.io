# Publishing Workflow

## Recommendation

Use GitHub Pages as the canonical publishing surface for Lacey's longform posts,
and use this repo as the editorial planning, provenance, and task-tracking home.

GitHub Pages can serve static files directly from a repository and can also run a
build through GitHub Actions. GitHub's current docs recommend Actions for
automation-heavy Pages sites, especially when the site needs a custom build
process. For a personal blog, the simplest strong setup is:

- Lacey owns a user site repository named `<owner>.github.io`, or a project repo
  with Pages enabled.
- The site uses Jekyll, Astro, Hugo, or another static generator.
- Posts live as Markdown with front matter.
- GitHub Actions builds and deploys the site.
- This repo tracks ideas, source provenance, draft status, and social variants.

Sources checked on 2026-07-01:

- GitHub Pages hosts static HTML, CSS, and JavaScript from a repository and can
  optionally run a build process.
- Pages can publish from a branch or through GitHub Actions.
- GitHub's Jekyll docs state that GitHub Actions is now the recommended approach
  for deploying and automating Pages sites.
- Pages sites are public on the internet, so drafts and sensitive notes should
  not be placed in a publishing repo unless they are meant to be public.

## Why Not Put Everything In Lacey's Blog Repo?

Keep this repo as the backstage system because it can contain:

- issue backlog and editorial planning;
- provenance notes from PsychSimulator and Psych-LLM-Wiki;
- unpublished topic maps;
- social copy variants;
- product-launch sequencing;
- review checklists.

The public blog repo should contain only publishable posts, public assets, and
site code.

## Recommended Repo Layout For Lacey's Blog

For a Jekyll Pages site:

```text
_config.yml
_posts/
  2026-07-12-why-that-email-felt-like-a-trap.md
assets/
  images/
pages/
  about.md
  resources.md
```

For Hugo or Astro:

```text
content/
  posts/
    why-that-email-felt-like-a-trap.md
src/ or layouts/
public/ or dist/
.github/workflows/pages.yml
```

Jekyll is easiest if Lacey wants the least infrastructure. Hugo or Astro is
better if the site will later need richer design, reusable post cards, embedded
interactive pieces, or a more polished brand system.

## Editorial Issue Lifecycle

Use one GitHub issue per post.

Statuses:

- `idea`: title, hook, concept, source candidates.
- `outline`: scene, concept, reader takeaway, provenance.
- `draft`: longform draft exists.
- `review`: Lacey academic/voice review.
- `ready`: scheduled and social variants prepared.
- `published`: live URL, cross-post URLs, notes.

## Drafting Flow

1. Create an issue from `.github/ISSUE_TEMPLATE/blog_post.md`.
2. Attach concept and source IDs from `docs/provenance-map.md`.
3. Draft from `docs/draft-template.md`.
4. Review against the quality checklist in `docs/editorial-strategy.md`.
5. Move the final Markdown into Lacey's Pages repo.
6. Publish with GitHub Actions.
7. Add the live URL and social links back to the issue.

## Social Distribution

For each longform post, create:

- LinkedIn: 600-1,200 characters, one professional story, one reflection prompt.
- Instagram: 5-7 slide carousel or 90-second reel script, one concept per slide.
- Facebook: warmer, community-oriented excerpt with a question at the end.

Do not post the exact same copy everywhere. Keep the same concept and example,
but tune the opening and call to conversation for the platform.

## Governance Notes

- Posts are educational, not therapy, diagnosis, or treatment.
- If a post discusses distress, trauma, attachment, coping, or schemas, include a
  plain-language boundary note where appropriate.
- Avoid exposing private simulator examples or Lacey's personal profile fixture.
- Do not imply the simulator can diagnose, predict, or replace clinical judgment.
