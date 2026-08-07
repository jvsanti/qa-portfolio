# Global Lives Project — Bugs Found

![env](https://img.shields.io/badge/ENV-Real_Production-brightgreen?style=flat-square) `globallives.org`

---

### `GLP-001` Date of birth contradicts bio text

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Open Rumi Nagashima's profile
2. Compare the Date of Birth field with the biography text

**Expected:** Date of Birth field should match the year stated in the biography (1984).

**Actual:** Field says 1982. Same pattern found on Dušan Lazić's profile: field says 1952, bio says 1942 (10-year discrepancy).

---

### `GLP-002` Sign Up / Log In forms active despite banner

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Note the site banner stating all submission forms are turned off
2. Try the Sign Up and Log In forms anyway

**Expected:** Forms should be disabled/inactive, matching the banner.

**Actual:** Both forms remain fully accessible and functional.

---
