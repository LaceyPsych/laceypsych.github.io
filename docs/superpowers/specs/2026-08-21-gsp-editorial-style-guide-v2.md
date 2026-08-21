# GSP Editorial Style Guide V2 Spec

Date: 2026-08-21

Source issue: https://github.com/LaceyPsych/laceypsych.github.io/issues/103

## Goal

Implement the Generative Systems Psychology editorial style guide v2 as a
repo-local publishing standard and apply it to the current blog archive.

The standard should persist in future blogs through reusable docs, templates,
and issue checklists. Existing published posts should receive focused editorial
adjustments only where needed to clarify GSP terminology, generated-output
logic, accountability, source boundaries, or public safety.

## Editorial Requirements

- Generative Systems Psychology is the organizing framework.
- Psychological Architecture remains a construct within GSP, not a replacement
  framework name.
- Each post teaches one primary concept.
- Each post begins with an ordinary human scene.
- Each post locates its core concept inside GSP.
- Each post makes the relevant generated-output pathway visible.
- Each post preserves accountability and avoids determinism.
- Established research supports GSP without replacing it as the explanatory
  frame.
- Public examples remain fictional, composite, nonclinical, and reader-safe.

## Existing Post Audit

- `A Person Is an Architecture Under Pressure`: broad opening essay; preserve
  the title and construct language while naming the GSP frame more explicitly.
- `The Apology Draft That Became a Dissertation`: strengthen GSP location for
  needs, schemas, regulation, and generated output; keep the warm repair-focused
  voice.
- `Your Spreadsheet Is Trying To Protect You`: strengthen GSP location for
  appraisal, Psychological Architecture, feedback, and generated-output pathway.
- `Behavior Is the Smoke, Not the Fire`: keep the generated-output thesis;
  tighten GSP framing and line wrapping.

## Future Publishing Infrastructure

- Create a canonical editorial guide at `docs/editorial-style-guide.md`.
- Link the canonical guide from `README.md`.
- Update `docs/draft-template.md` with GSP metadata, pathway, accountability,
  public-safety, and style-guide checks.
- Update `.github/ISSUE_TEMPLATE/blog_post.md` so new blog issues inherit the
  v2 editorial requirements.
- Keep superpowers spec and plan files for this issue.

## Acceptance Criteria

- A v2 editorial guide exists and reflects issue #103.
- A matching superpowers execution plan exists.
- All published posts have been reviewed and lightly edited where needed.
- Future blog scaffolding requires GSP concept, pathway, accountability, and
  safety checks.
- Hugo build passes locally.
- The PR references issue #103.
