# Cinks Labs — Bugs Found

![env](https://img.shields.io/badge/ENV-Real_Production-brightgreen?style=flat-square) `cinkslabs.com`

---

### `CNK-001` Phone field accepts invalid input

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to the Contact Us page
2. Enter a non-numeric/invalid value in the Phone Number field
3. Submit

**Expected:** Form should validate phone number format before submission.

**Actual:** Form submits successfully with no format validation.

---

### `CNK-002` Blog comment field has no character limit

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Open a blog post
2. Enter an extremely long comment
3. Submit

**Expected:** A reasonable character limit should be enforced.

**Actual:** Comment is accepted with no limit, breaking the page layout (extreme page length).

---
