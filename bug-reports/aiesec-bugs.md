# AIESEC (aiesec.org) — Bugs Found in Production

Real bugs found on a live production website (not a training app), during exploratory testing of the public site.

**Bug 1 — Minor.** Typo in the "We create value-driven leaders" homepage section.
- Steps: Go to AIESEC → scroll to that section.
- Expected: "AIESEC enables you to develop the values we believe leaders should live by."
- Actual: "...develop **thev** values..." (typo: "thev" instead of "the").

**Bug 2 — Minor.** Typo/duplication in the "Premium Global Partners" paragraph, Global Talent page.
- Steps: Go to /global-talent → scroll to the paragraph below "AIESEC's Premium Global Partners are top organizations...".
- Expected: "...present in different Countries/Territories around the world."
- Actual: "...present in different Countries/Territories **and territiories** around the world" (misspelled + redundant word).
