# ADR-001: Preserve the current information architecture

- **Status:** DECIDED
- **Date:** 2026-10-04
- **Scope:** square18.it public frontend

## Context

The current website follows a compact navigation model:

**Home → Menu → category pages**

The October 2026 audit found that the main navigation path was understandable and that tested internal links did not reveal unexpected 404 responses or redirects.

The audit did identify specific defects in performance, accessibility, semantics and public-information consistency, but it did not produce evidence that the overall information architecture itself was the problem.

## Decision

Preserve the current information architecture and improve it incrementally.

In particular:

- keep the Home page short;
- keep the Menu as the central hub;
- keep category-based navigation;
- keep the primary menu in HTML rather than replacing it with a PDF;
- preserve the current visual identity unless a verified usability or accessibility problem requires change;
- prioritize mobile behaviour when trade-offs are necessary.

## Rationale

A structural redesign would add cost and regression risk without addressing the highest-priority verified problems.

The current backlog is better served by targeted work on:

- image performance;
- keyboard accessibility;
- semantic HTML;
- public information consistency;
- technical SEO verification;
- responsive QA.

## Consequences

### Positive

- lower regression risk;
- less unnecessary design churn;
- faster delivery of measurable improvements;
- continuity for returning users;
- simpler maintenance.

### Trade-offs

- existing design constraints remain in place;
- improvements must often work within the current Elementor structure;
- a future redesign remains possible if evidence later shows that the architecture itself limits usability or maintainability.

## Review trigger

Revisit this decision only if future evidence shows that the existing architecture creates measurable navigation, conversion, accessibility or maintenance problems.

## Evidence state

- Current navigation structure: **VERIFIED**
- Need for full redesign: **NOT DEMONSTRATED**
- Decision to preserve architecture: **DECIDED**
