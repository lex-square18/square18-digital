# square18-digital

Technical case study and development log for **square18.it**.

This repository documents selected engineering, UX, accessibility, performance and SEO work carried out on the public website of sQuare.

It is not a source-code mirror or WordPress backup.

## Project goal

The website is being developed as a small, maintainable, mobile-first public interface where operational information can be kept clear and consistent.

The target information architecture is centred on:

**Menu → prices → ingredients / allergens → opening information → location → contacts**

The project deliberately favours correctness, speed and maintainability over feature growth.

## Current approach

Changes are made incrementally:

1. observe the current behaviour;
2. identify a measurable problem;
3. assess regression risk;
4. make the smallest effective change;
5. verify the real result;
6. record the outcome.

A change is not considered complete merely because it has been implemented.

Typical states used in this repository include:

- `VERIFIED`
- `HIGH-CONFIDENCE`
- `REQUIRES VERIFICATION`
- `PROPOSAL`
- `DECIDED`
- `IMPLEMENTED`
- `VERIFIED IMPLEMENTED`
- `SUPERSEDED`

## Current verified work areas

The October 2026 audit identified several concrete improvement areas, including:

- an oversized Home hero image;
- menu cards that are clickable with a pointer but are not correctly exposed in keyboard navigation;
- missing accessible names on some icon links;
- heading and landmark semantics that need refinement;
- public information that requires reconciliation before being treated as canonical.

Other areas, including structured-data coverage and some SEO configuration, remain explicitly marked for verification rather than being reported as missing.

## What this repository may contain

- sanitized technical audits
- decision records
- measured before / after results
- accessibility findings
- implementation notes
- experiments
- technical issues
- selected screenshots that have passed privacy and security review

## What this repository will not contain

- WordPress backups
- database exports
- production credentials
- `.env` files
- real `wp-config.php`
- API keys or tokens
- session data or cookies
- private emails
- internal financial or commercial information
- employee or customer personal data
- confidential documents
- unnecessary production infrastructure details

See `SECURITY.md` for the publication policy.

## Current priorities

The current technical backlog prioritizes:

1. Home hero image optimization;
2. keyboard accessibility of menu cards;
3. reconciliation of canonical public information;
4. accessible naming and semantic structure;
5. essential page completeness;
6. technical SEO verification;
7. final responsive and performance QA.

The project does not currently assume that more features are better. Features such as chatbots, popup systems, social widgets, embedded maps or a replacement PDF menu require a demonstrated use case before being considered.

## Website

https://www.square18.it/

---

Built as a living technical record, not as a production infrastructure mirror.
