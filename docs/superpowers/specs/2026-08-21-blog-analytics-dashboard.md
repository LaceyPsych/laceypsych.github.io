# Blog Analytics Dashboard Spec

Date: 2026-08-21

Source issue: https://github.com/LaceyPsych/laceypsych.github.io/issues/100

## Goal

Create a repo-local analytics dashboard for published Generative Systems
Psychology posts and make analytics part of the publishing workflow for future
blogs.

The dashboard should track views, followers, engagement, social performance,
reader feedback, arc-level performance, and editorial learnings. It should also
preserve the v2 editorial style standard: analytics may guide presentation and
sequencing, but it must not distort GSP concepts, accountability, public safety,
or theoretical integrity.

## Current Blog Baseline

Seed the dashboard with the four published posts:

- `A Person Is an Architecture Under Pressure`
- `The Apology Draft That Became a Dissertation`
- `Your Spreadsheet Is Trying To Protect You`
- `Behavior Is the Smoke, Not the Fire`

Real analytics data is not present in the repository, so numeric metrics should
use `TBD` placeholders rather than invented counts.

## Implementation Requirements

- Add `docs/blog-analytics-dashboard.md`.
- Link the dashboard from README operating docs.
- Add analytics update steps to `docs/publishing-workflow.md`.
- Add post-publication analytics fields to `.github/ISSUE_TEMPLATE/blog_post.md`.
- Include an editorial-style compliance section so prior and future posts are
  checked against `docs/editorial-style-guide.md`.
- Use current GSP terminology, not the previous framework name.
- Add a matching superpowers execution plan.

## Acceptance Criteria

- Dashboard includes overall metrics, blog performance, follower tracking,
  traffic sources, social performance, top performers, arc performance, reader
  response, editorial findings, future experiments, and a new-post metrics
  template.
- Dashboard includes all currently published posts.
- Dashboard explicitly states that analytics must not distort GSP.
- Future blog issues include analytics and editorial-learning fields.
- Hugo build passes.
