# EnergyTelecom — Bugs Found (energy-telecom.portnov.com)

**Moderate.** "My monthly bill is approximately" field applies a phone-number input mask instead of accepting a dollar amount.
Steps: Cell Phone Service section → type a numeric value into the "$" field. Actual: input reformatted as a phone number (e.g. "+1 (289) 854-1"). Expected: plain dollar amount accepted.

**Moderate.** "Total Bill" field (Local/Long Distance/International Service) accepts non-numeric text with no validation.
Steps: type letters (e.g. "Tenetur quo") into the "Total Bill: $" field. Actual: text accepted and displayed, no error.

**Minor.** Typo in the Gas and Electric Services checkbox label: "I am **opento** using different provider" (missing space) — expected "open to".
