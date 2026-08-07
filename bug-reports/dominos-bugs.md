# Domino's Brasil — Bugs Found (dominos.com.br) — Real Production Site

**DOM-001 — Major / High priority.** Cart page does not enforce a product quantity limit, eventually breaking checkout.
Steps: add a product → repeatedly increase quantity via "+" well beyond a normal order size. Actual: error modal "Ops! Algo deu errado" (error code PLS-JFT5SR4) appears, and Subtotal/Total values stop updating. Expected: a reasonable maximum quantity per item should be enforced before the app breaks.

**DOM-002 — Minor / Low priority.** "PIZZA GRANDE R$44,90/CADA" promotion description contains a duplicated word ("ou ou monte" instead of "ou monte").
