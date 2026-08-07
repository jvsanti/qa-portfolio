# Conduit (RealWorld app) — Bugs Found

**Minor.** Every article in the Global Feed shows the same posting date ("August 3rd") regardless of actual publish date.

**Minor.** Avatar becomes a broken image after updating "URL of profile picture" with a non-URL value (e.g. "teste") — no validation, no fallback to previous avatar.

**Major.** Registration form accepts clearly invalid username/email/password formats (e.g. username "@@", email "!@1", password ".") with zero validation — account gets created anyway.
