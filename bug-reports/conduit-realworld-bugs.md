# Conduit (RealWorld app) — Bugs Found

![env](https://img.shields.io/badge/ENV-Training_App-lightgrey?style=flat-square) `realworld reference app`

---

### `CND-001` All articles show the same publish date

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Open the Global Feed
2. Compare the posting date shown on each article

**Expected:** Each article shows its own publish date.

**Actual:** Every article shows the same date ("August 3rd") regardless of when it was actually published.

---

### `CND-002` Broken avatar on invalid profile picture URL

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to Settings
2. Enter a non-URL value (e.g. 'teste') in 'URL of profile picture'
3. Save

**Expected:** Should reject invalid input or fall back to the previous avatar.

**Actual:** Avatar becomes a broken image with no validation or fallback.

---

### `CND-003` Registration accepts invalid formats with zero validation

![Major](https://img.shields.io/badge/SEVERITY-MAJOR-orange?style=flat-square) `Priority: High`

**Steps to reproduce**
1. Go to Sign Up
2. Enter clearly invalid username/email/password (e.g. '@@' / '!@1' / '.')
3. Submit

**Expected:** Form should validate username, email, and password formats.

**Actual:** Account is created successfully despite invalid input in all three fields.

---
