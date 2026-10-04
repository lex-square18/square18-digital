# ADR-002: No feature expansion without demonstrated need

- **Status:** DECIDED
- **Date:** 2026-10-04
- **Scope:** square18.it public frontend

## Context

The current project backlog contains several verified issues in performance, accessibility, semantics, content completeness and technical verification.

At the same time, there is no current evidence that the website requires additional feature layers such as:

- chatbots;
- promotional popups;
- newsletters;
- embedded social widgets;
- embedded maps;
- a PDF replacing the HTML menu;
- online booking;
- online ordering;
- heatmaps;
- large technology migrations.

Each additional feature adds some combination of maintenance cost, page weight, privacy considerations, operational complexity or dependency risk.

## Decision

Do not add new feature classes unless there is a demonstrated user or operational need.

A feature should be considered only when at least one of the following exists:

- a verified user problem;
- a recurring operational problem;
- measurable demand;
- a clear business process that the feature improves;
- evidence that the expected benefit exceeds implementation and maintenance cost.

## Rationale

The current website is intentionally small.

The highest-value work is to make the existing system more correct, accessible, fast and maintainable before increasing its surface area.

Feature count is not a project KPI.

## Consequences

### Positive

- lower maintenance burden;
- fewer third-party dependencies;
- lower privacy and performance risk;
- clearer prioritization;
- easier QA.

### Trade-offs

- some potentially useful features will be deferred;
- future requests require evidence rather than being accepted by default.

## Review trigger

Revisit an excluded feature when a concrete requirement, repeated user need or measurable business case appears.

## Evidence state

- Current technical backlog: **VERIFIED**
- Need for the listed feature expansion: **NOT DEMONSTRATED**
- Decision to require evidence before expansion: **DECIDED**
