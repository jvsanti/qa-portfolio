# Domino's Brazil — Bugs Found

![env](https://img.shields.io/badge/ENV-Real_Production-brightgreen?style=flat-square) `dominos.com.br`

Real production e-commerce site.

---

### `DOM-001` Cart has no quantity cap — checkout breaks

![Major](https://img.shields.io/badge/SEVERITY-MAJOR-orange?style=flat-square) `Priority: High`

**Steps to reproduce**
1. Add a product to the cart
2. Repeatedly increase quantity via the '+' button well beyond a normal order size

**Expected:** The cart enforces a reasonable maximum quantity per item before the total breaks.

**Actual:** Error modal 'Ops! Algo deu errado' appears (error code PLS-JFT5SR4), and Subtotal/Total stop updating.

---

### `DOM-002` Duplicated word in promo description

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Low`

**Steps to reproduce**
1. Open the homepage
2. Read the 'PIZZA GRANDE R$44,90/CADA' promotion description

**Expected:** "...ou monte sua própria pizza..."

**Actual:** Duplicated word: "...ou **ou** monte..."

---
