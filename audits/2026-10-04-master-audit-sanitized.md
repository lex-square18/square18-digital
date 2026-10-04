# square18.it — Sanitized Technical Audit

**Audit date:** 2026-10-04  
**Publication status:** VERIFIED SAFE TO PUBLISH  
**Scope:** public frontend behaviour and selected external performance measurements

This document is a sanitized public extract of the project audit. It intentionally excludes private correspondence, internal business data, credentials, production configuration and nonessential infrastructure details.

## Method

The audit combined rendered-browser inspection, keyboard interaction tests and PageSpeed Insights / Lighthouse observations.

Evidence states are kept explicit:

- **VERIFIED**: directly observed or measured.
- **HIGH-CONFIDENCE**: strong evidence, but incomplete verification.
- **REQUIRES VERIFICATION**: not demonstrated by the available inspection.
- **BLOCKED**: requires a canonical business decision or missing source.
- **PROPOSED**: recommended but not yet implemented.
- **VERIFIED IMPLEMENTED**: implemented and subsequently tested.

An automated Lighthouse score is not treated as WCAG certification, and laboratory performance data is not treated as equivalent to real-user field data.

## Architecture worth preserving

**VERIFIED**

The tested navigation follows a compact path:

**Home → Menu hub → category pages**

The baseline browser test reached the Menu categories and the tested nested Gin & Tonic path. Tested internal navigation produced no unexpected 404 or redirect.

The current direction is therefore incremental improvement rather than structural redesign.

## Performance

### Home hero image

**VERIFIED ISSUE**

Lighthouse identified the Home hero background PNG at approximately **13.7 MiB**. In the mobile run, total measured payload was approximately **14,296 KiB** and the report estimated that image optimization could save roughly **13,141 KiB**.

This makes the hero asset the clearest immediate payload optimization target.

### PageSpeed snapshot

PageSpeed Insights test on 2026-10-04, approximately 04:40 CEST:

| Metric | Mobile | Desktop |
| --- | ---: | ---: |
| Lighthouse Performance | 64 | 71 |
| FCP | 3.5 s | 0.8 s |
| LCP | 73.6 s | 12.0 s |
| TBT | 0 ms | 0 ms |
| CLS | 0.043 | 0.041 |
| Approx. payload | 14,296 KiB | 14,311 KiB |

These are laboratory measurements from a test session, not timings observed for every visitor.

The mobile CrUX data shown by PageSpeed passed the Core Web Vitals assessment, with LCP around **2 s**, CLS **0**, and INP unavailable. No desktop field data was available in that snapshot. The available mobile field result appeared to be origin-level rather than evidence for every individual page.

**Conclusion:** lab and field measurements must remain separate. The oversized image is independently actionable even though simulated LCP and available field data differ sharply.

## Accessibility

### Menu cards

**VERIFIED ISSUE**

The Menu category cards worked with pointer interaction, but keyboard testing skipped them during Tab navigation.

Because these cards form the primary Menu navigation, the intended correction is to make the complete card a semantic link while preserving its existing appearance.

Verification after implementation should include:

- Tab and Shift+Tab;
- Enter activation;
- visible focus;
- pointer interaction;
- touch interaction;
- responsive regression checks.

### Accessible names and semantics

**VERIFIED ISSUES**

The audit also observed:

- icon links without accessible names;
- discontinuous heading hierarchy;
- absence of a main `<main>` landmark in the inspected structure.

These should be corrected without unnecessary visual redesign.

Lighthouse returned an accessibility score of 92 in the tested mobile and desktop runs, but this does not establish WCAG conformance.

## Responsive behaviour

**PARTIALLY VERIFIED**

Home, Menu and a representative category were inspected at multiple widths without evidence of a generalized overflow problem.

The audit did **not** verify every page at every target viewport. Full responsive QA therefore remains open.

Project QA targets are:

- 375 / 390 px
- 430 px
- 768 px
- 1024 px
- 1440 px

## Navigation and external actions

**VERIFIED**

Tested internal navigation did not reveal unexpected 404 responses or redirects.

The browser environment could not launch the `tel:` protocol. This is recorded as a **tool limitation**, not as a website defect.

Tested Maps and social destinations reached their declared targets.

## SEO and metadata

### Verified

Descriptive page titles were present on inspected pages. The Home PageSpeed report flagged a missing meta description.

### Requires verification

The audit did not directly verify:

- canonical tags;
- sitemap;
- robots.txt;
- structured data coverage;
- Open Graph metadata;
- current indexing of historical URLs.

These items must not be reported as absent merely because the audit tooling could not inspect them.

## Public information consistency

**VERIFIED ISSUE / BLOCKED DECISION**

Opening information differed between public channels during the audit.

The technical action is not to guess the correct schedule. A canonical schedule must first be approved and then synchronized across the website and relevant external profiles.

The broader product goal is for the website to become the canonical public source for:

**Menu → prices → ingredients / allergens → opening information → location → contacts**

## Current priority order

1. Optimize the 13.7 MiB Home hero.
2. Make Menu cards keyboard accessible.
3. Establish and synchronize canonical opening information.
4. Remove the generic site-update notice.
5. Reconcile canonical public contact information.
6. Correct heading structure, main landmark and accessible names.
7. Complete essential About content.
8. Complete essential Contact content.
9. Verify technical SEO.
10. Run final performance and responsive QA.

## Deliberate non-goals

No evidence from this audit establishes a need for a chatbot, popup system, newsletter, social widget, embedded map, PDF as the primary menu, booking system, ordering system or major technology migration.

New complexity should require a demonstrated operational or user benefit.

## Verification limits

This audit did not constitute:

- WCAG certification;
- legal/privacy compliance certification;
- security certification;
- exhaustive testing of every viewport and page;
- complete network/storage inspection;
- Search Console analysis;
- full backend inspection.

The objective is a traceable engineering backlog, not an inflated compliance claim.
