# Lacey Pages Setup Runbook

Issue: #5

## Decision

Use `LaceyPsych/laceypsych.github.io` as Lacey's public GitHub Pages site, built
with Hugo and deployed with GitHub Actions.

Public repo:

```text
https://github.com/LaceyPsych/laceypsych.github.io
```

Default Pages URL:

```text
https://laceypsych.github.io/
```

Canonical public domain:

```text
https://lacey.life/
```

## Why Hugo

Hugo is the better fit for this project because the blog is intended to become a
serious branded publication, not only a lightweight personal notes page:

- Markdown posts map directly to the editorial workflow in this repo.
- Fast builds keep GitHub Actions deploys cheap and predictable.
- Sections, taxonomies, tags, and series are first-class enough for a long-term
  editorial archive.
- The content model can grow into essays, resources, explainers, and future
  simulator launch pages without changing platforms.
- Hugo can be built with GitHub Actions and deployed to GitHub Pages without
  committing generated `public/` output.

The starter template has been promoted to the repository root so GitHub Actions
can build the site directly from `main`.

## Repository Boundary

Lacey's Pages repo contains public-ready site material and the public editorial
issue tracker:

- `content/posts/` Markdown posts;
- public pages such as About and Resources;
- images/assets approved for publication;
- site config and GitHub Actions workflow.

Do not copy private simulator fixtures, unpublished profile notes, or internal
planning files into the public Pages repo.

## Setup Steps

1. Keep `hugo.toml` pointed at `https://lacey.life/`.
2. Keep `CNAME` set to `lacey.life`.
3. Enable GitHub Pages:
   - repository Settings;
   - Pages;
   - Source: GitHub Actions.
4. Merge publishing PRs into `main`.
5. Confirm the Pages workflow deploys.
6. Add the published URL back to the matching issue.

## Custom Domain

The target domain is `lacey.life`. If both apex and `www` are available, prefer
serving the canonical public site at the apex and redirecting `www` to it, unless
GitHub Pages DNS constraints make `www.lacey.life` the simpler first launch.

DNS should point `lacey.life` at GitHub Pages and redirect or alias
`www.lacey.life` to the canonical apex. Add the custom domain through GitHub
repository Settings rather than relying only on the `CNAME` file.

## First Publish Test

The first publish test is the post from
`LaceyPsych/laceypsych.github.io#2`, "A Person Is an Architecture Under
Pressure."

Checklist:

- [ ] Default Pages URL loads.
- [ ] Home page lists the first post.
- [ ] Post page renders title, date, tags, and content.
- [ ] About page renders.
- [ ] Resources page renders.
- [ ] RSS feed is generated.
- [ ] No internal repo paths or private source notes are visible.
- [ ] Source issue is updated with the live URL.

## Remaining Decisions

These require user/Lacey input before launch is complete:

- DNS records for `lacey.life`.
- GitHub Pages custom domain verification.
- Public display bio refinements.
- Social profile URLs.
