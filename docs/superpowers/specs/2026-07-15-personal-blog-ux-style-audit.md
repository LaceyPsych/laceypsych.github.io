# Personal Blog UX Style Audit Spec

Date: 2026-07-15

Repo: `LaceyPsych/laceypsych.github.io`

## Goal

Define the next design pass for Lacey's personal psychology blog after the first
post has merged. The site should remain a personal, quiet, text-first blog, but
it needs stronger orientation, trust signals, and longform reading support for a
psychology and therapy-adjacent audience.

This is a spec only. Do not implement visual changes from this document without
a follow-up issue or PR.

## Research Inputs

UX and health-literacy sources reviewed:

- NN/g, "How Users Read on the Web" (scannable text, meaningful subheads,
  objective language, outbound links for credibility).
- NN/g, "F-Shaped Pattern of Reading on the Web" (users scan when pages lack
  formatting cues; good design should guide attention instead of letting the
  default F-pattern dominate).
- NN/g, "Legibility, Readability, and Comprehension" (large default type, high
  contrast, clean typefaces, plainspoken words, short sentences, active voice).
- NN/g, "Trustworthiness in Web Design" (design quality, upfront disclosure,
  comprehensive content, and connection to the rest of the web).
- HHS/ODPHP Health Literacy Online, 3rd edition (people-first design,
  accessibility, actionable content, easy scanning, simple navigation, content
  governance).
- Public psychology publisher pattern scan:
  - Verywell Mind foregrounds category navigation, editorial process, review
    board, crisis support, and a medical-advice boundary.
  - Greater Good Magazine foregrounds topic taxonomy, practical resources,
    science framing, newsletter, and institutional credibility.
  - The Gottman blog foregrounds relationship domain pathways, quizzes/tools,
    and professional/service context.

## Current Repo Audit

Strengths:

- The site is fast, static, and quiet.
- The reading column is constrained to `760px`, which supports longform essays.
- Default body type is large (`18px`) with generous line height (`1.65`).
- Navigation is simple: Posts, About, Resources.
- The first post includes public source links and an educational boundary note.
- Hugo, CNAME, and GitHub Pages Actions are in place.

Gaps:

- The home page lacks a clear editorial promise beyond one sentence.
- There is no visible author credential/context block near posts.
- The boundary note exists inside the first post, but there is no site-wide
  disclaimer pattern.
- The Resources page is a placeholder, so source credibility is not yet carried
  by a real public resource library.
- Post pages do not show summary, series, reading time, source/provenance links,
  or next/previous navigation.
- Tags are visually present but not linked as taxonomy paths.
- There is no newsletter, RSS prompt, or lightweight "keep reading" path.
- There is no emergency/crisis-support signpost. The site should not become a
  crisis resource, but psychology-adjacent publishing needs a visible boundary.
- The visual system reads as a good bare starter theme, not yet as a distinctive
  personal blog for Lacey.

## Design Direction

The best fit is **warm editorial minimalism**:

- text-first;
- low visual noise;
- generous whitespace;
- warmer typographic hierarchy;
- clear source and boundary signals;
- a few human, memorable moments rather than stock therapy imagery;
- no marketing hero, decorative gradient, or therapy-sales landing page.

The site should feel like a trusted notebook from a precise, humane thinker:
easy to read on a phone, credible enough for psychology-adjacent claims, and
personal enough that it does not read like a content farm.

## Information Architecture

Recommended top navigation:

- `Posts`
- `Series`
- `Resources`
- `About`

Add only when content exists:

- `Newsletter`
- `Contact`

Home page structure:

1. Editorial promise:
   - "Plain-language essays on psychology, relationships, work, and the systems
     that shape behavior under pressure."
2. Latest post feature:
   - title, date, summary, tags/series, primary link.
3. Start here:
   - Human Architecture Theory;
   - Relationships and repair;
   - Work and pressure;
   - Parenting and attachment;
   - Body, stress, and constraint.
4. Boundary note:
   - educational reflection, not therapy or crisis care.
5. Recent posts.

Post page structure:

1. Title.
2. Deck/summary.
3. Meta row:
   - date;
   - reading time;
   - series;
   - educational boundary link.
4. Body.
5. "A small question" or "Try this lens" callout.
6. Sources and further reading.
7. Series navigation / next post.

Resources page:

- Group sources by reader need, not by internal graph taxonomy:
  - Understanding stress and access;
  - Relationships and attachment;
  - Emotion and coping;
  - Needs and motivation;
  - Decision-making under pressure;
  - Responsible simulation and AI.
- Each resource gets one-sentence plain-language relevance.
- Avoid dumping source IDs publicly unless paired with readable labels.

## Visual System

Typography:

- Keep body at `18px` minimum.
- Use a readable serif for article titles and body, or keep system sans for body
  and add a restrained serif only for headings. Test both.
- Keep line length around the current `680-760px` max for article text.
- Add more distinct `h2`/`h3` styling so long essays are easier to scan.
- Add blockquote styling for narrative dialogue and "small question" sections.

Color:

- Keep the warm off-white background.
- Keep teal/green as a trust accent, but add one secondary warm accent for
  callouts.
- Avoid beige-only drift; the palette should not become a tan therapy template.
- Maintain high text/background contrast.

Layout:

- Preserve one-column article reading.
- Use full-width bands only for home-page orientation sections, not nested cards.
- Cards are acceptable for repeated post summaries only.
- Avoid decorative clinical stock photos.

Components:

- Site-wide boundary/disclaimer block.
- Post summary/deck.
- Linked tags and series chips.
- Source list component.
- "Start here" topic list.
- Newsletter/RSS prompt.
- Next/previous post navigation.
- Accessible skip link.

## Trust And Safety Requirements

Every page should make these things easy to discover:

- Who is writing.
- What the site is and is not.
- Whether the content is educational, clinical, personal, or source-backed.
- Where sources live.
- What to do if someone is in immediate danger or crisis.

Do:

- Use calm, specific boundary language.
- Link to source material when making research claims.
- Show dates and update dates when content changes materially.
- Keep sensitive posts framed as reflection and education.

Do not:

- Present posts as diagnosis, treatment, or individualized advice.
- Use testimonials or client-like stories.
- Use urgency-based newsletter language.
- Overload the header with services before the blog voice is established.

## Implementation Plan

Phase 1: Foundation

- Add a site-wide boundary component in the footer or post template.
- Add skip link and basic focus styles.
- Add post `summary`, reading time, and series display.
- Make tags link to taxonomy pages.
- Add next/previous post navigation.
- Expand the Resources page from placeholder to curated source guide.

Phase 2: Home And Archive

- Rebuild the home page as an editorial entry point, not just a post list.
- Add "Start here" topic pathways.
- Add a featured latest post treatment.
- Add a simple Series page.

Phase 3: Visual Refinement

- Tune type scale, heading rhythm, blockquotes, callouts, and source lists.
- Add a restrained secondary accent.
- Add print styles for posts.
- Test mobile reading, long titles, and source-heavy posts.

Phase 4: Trust And Distribution

- Add RSS/newsletter affordance.
- Add author/context block.
- Add update-date support.
- Add Open Graph/Twitter card metadata.
- Add JSON-LD only if it remains accurate and low-maintenance.

## Acceptance Criteria For The Design PR

- `hugo --minify` passes.
- Home, post, posts list, about, resources, tag, and series pages render cleanly.
- Mobile width `360px` has no horizontal scrolling.
- Body text remains at least `18px`.
- Links and focus states are visible.
- Posts include clear boundary and source patterns.
- Tags are navigable.
- The site still feels like a personal writing archive, not a therapy practice
  landing page or generic wellness magazine.

## Open Questions

- Should the public author name stay "Lacey" only, or should About include full
  credentials/licensure context?
- Should the site include a newsletter now, or wait until three to five posts
  exist?
- Should crisis-support links be national-only or location-aware? If added, use
  a maintained source rather than hard-coding broad hotline claims.
- Should images be avoided entirely for now, or should each series get a subtle
  reusable visual motif?
