# Security Policy

## Public repository scope

This repository contains sanitized technical documentation relating to the public website square18.it.

It is not a production infrastructure repository.

## Never publish

The following material must never be committed, attached to an issue, added to a discussion or included in a screenshot:

- passwords;
- one-time passwords;
- passkeys or recovery codes;
- API keys;
- access tokens;
- secrets;
- cookies or session identifiers;
- SSH private keys;
- `.env` files;
- production `wp-config.php`;
- SMTP credentials;
- database dumps;
- backups;
- banking or payment data;
- tax documents;
- confidential contracts or legal material;
- private customer, employee or supplier data;
- private email or correspondence;
- identity documents;
- private addresses or telephone numbers;
- health information;
- software licence keys;
- private analytics identifiers;
- administrative URLs containing credentials or tokens;
- unnecessary production topology or configuration details.

Partially masked secrets should not be published when the remaining information could still create risk.

## Screenshots

Screenshots require full-image inspection before publication.

Review must include browser tabs, address bar, query parameters, account avatars and names, email addresses, notifications, bookmarks, side panels, developer tools and background applications.

When in doubt, do not publish the screenshot.

## Publication gate

Every public artifact should pass:

**SECURITY REVIEW:** PASS / FAIL  
**SENSITIVE DATA:** NONE / DETECTED / UNCERTAIN  
**FACT CHECK:** PASS / PARTIAL / FAIL

Only content with final status **VERIFIED SAFE TO PUBLISH** may be published.

Otherwise use **DO NOT PUBLISH — REQUIRES REVIEW** or **BLOCKED — SENSITIVE DATA DETECTED**.

## Vulnerability reports

Do not disclose potentially exploitable vulnerabilities through public issues before they have been evaluated.

Public documentation may describe security hardening after it is safe to do so, but should avoid unnecessary attack details or private infrastructure information.

## General rule

If information is not necessary to understand the public technical work, it should normally remain private.
