# Lacey Pages Setup Runbook

Issue: #5

## Decision

Use a dedicated GitHub Pages site for Lacey's public blog, built with Hugo and
deployed with GitHub Actions.

Recommended public repo:

```text
<lacey-github-owner>/<lacey-github-owner>.github.io
```

Use a project Pages repo only if Lacey already has a user site and wants the blog
under a subpath. A user site is cleaner for personal branding because the default
URL is the brand surface:

```text
https://<lacey-github-owner>.github.io/
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

Use the template in [templates/hugo-pages](../templates/hugo-pages/) as the
starting point for the public blog repo.

## Repository Boundary

This outreach repo remains private/backstage editorial infrastructure:

- roadmap and issue backlog;
- draft planning;
- source/provenance notes;
- social variants;
- product sequencing.

Lacey's Pages repo contains only public-ready site material:

- `content/posts/` Markdown posts;
- public pages such as About and Resources;
- images/assets approved for publication;
- site config and GitHub Actions workflow.

Do not copy private simulator fixtures, unpublished profile notes, or internal
planning files into the public Pages repo.

## Setup Steps

1. Create `<lacey-github-owner>.github.io` under Lacey's GitHub account.
2. Copy the contents of `templates/hugo-pages/` into that repo.
3. Update `hugo.toml`:
   - `title`
   - `baseURL`
   - `[params].description`
   - `[params.author].name`
   - `[params.author].bio`
   - social links
4. Enable GitHub Pages:
   - repository Settings;
   - Pages;
   - Source: GitHub Actions.
5. Push to `main` and confirm the Pages workflow deploys.
6. Add a custom domain only after the default `github.io` URL works.
7. Publish the first post by copying final Markdown into `content/posts/`.
8. Add the published URL back to the matching issue in this repo.

## Custom Domain

If Lacey owns a domain, prefer:

```text
www.<domain>
```

Use the apex domain only if DNS is managed carefully. Add the domain through
GitHub repository Settings rather than relying only on a `CNAME` file.

## First Publish Test

Use the sample post in the starter template only to verify deployment. Replace
it with the first reviewed outreach post before public launch.

Checklist:

- [ ] Default Pages URL loads.
- [ ] Home page lists the sample post.
- [ ] Post page renders title, date, tags, and content.
- [ ] About page renders.
- [ ] Resources page renders.
- [ ] RSS feed is generated.
- [ ] No internal repo paths or private source notes are visible.
- [ ] Issue #5 is updated with the live repo and URL.

## Remaining Decisions

These require user/Lacey input before issue #5 can be closed:

- Lacey's GitHub owner name.
- Public blog repo URL.
- Public display name and bio.
- Custom domain, if any.
- Social profile URLs.
