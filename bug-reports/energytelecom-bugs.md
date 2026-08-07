# EnergyTelecom — Bugs Found

![env](https://img.shields.io/badge/ENV-Real_Production-brightgreen?style=flat-square) `energy-telecom.portnov.com`

---

### `ENT-001` Phone mask applied to dollar-amount field

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Go to the Cell Phone Service section
2. Type a numeric dollar value into the '$' field

**Expected:** Plain dollar amount accepted, no reformatting.

**Actual:** Input is reformatted as a phone number (e.g. "+1 (289) 854-1").

---

### `ENT-002` Total Bill field accepts non-numeric text

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Go to Local/Long Distance/International Service
2. Type letters into the 'Total Bill: $' field

**Expected:** Field should reject non-numeric input.

**Actual:** Text (e.g. "Tenetur quo") is accepted and displayed with no error.

---

### `ENT-003` Missing space in checkbox label

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Go to Gas and Electric Services
2. Read the checkbox label

**Expected:** "I am open to using different provider"

**Actual:** "I am **opento** using different provider" (missing space).

---
