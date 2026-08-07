# AIESEC — Bugs Found

![env](https://img.shields.io/badge/ENV-Real_Production-brightgreen?style=flat-square) `aiesec.org`

Real bugs found on a live production website during exploratory testing of the public site.

---

### `AIESEC-001` Typo in homepage value-driven-leaders section

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to aiesec.org
2. Scroll to the 'We create value-driven leaders' section

**Expected:** "AIESEC enables you to develop the values we believe leaders should live by."

**Actual:** Typo: "...develop **thev** values..." instead of "the values".

---

### `AIESEC-002` Typo/duplication on Global Talent page

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to /global-talent
2. Scroll to the paragraph below 'AIESEC's Premium Global Partners...'

**Expected:** "...present in different Countries/Territories around the world."

**Actual:** "...present in different Countries/Territories **and territiories** around the world" (misspelled + redundant word).

---
