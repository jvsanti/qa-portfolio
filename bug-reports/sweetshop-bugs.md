# Sweet Shop — Bugs Found

![env](https://img.shields.io/badge/ENV-Training_App-lightgrey?style=flat-square) `sweetshop.netlify.app`

---

### `SWT-001` Broken 'About' link

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Go to the Basket page
2. Click the 'About' navigation link

**Expected:** Navigates to /about.

**Actual:** Points to a broken URL: /bout.

---

### `SWT-002` Social icons don't link anywhere

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to the Login page
2. Click any social media icon (Twitter, Facebook, LinkedIn)

**Expected:** Redirects to the respective social page.

**Actual:** All icons point to '#' — no redirect happens.

---
