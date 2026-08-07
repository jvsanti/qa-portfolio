# Test Design: Decision Table — Conduit "New Article" Form

Fields: Article title* / What's this article about* / Write your article* / Enter tags (optional). `*` = required.

16 combinations tested (1 false input, 2 false inputs, 3 false inputs), where PA = Publish Article, ER = Show error.

| TC | Title filled | Description filled | Body filled | Expected |
|---|---|---|---|---|
| TC1 | ✓ | ✓ | ✓ | PA |
| TC2 | ✗ | ✓ | ✓ | ER |
| TC3 | ✓ | ✗ | ✓ | ER |
| TC4 | ✓ | ✓ | ✗ | ER |
| TC5 | ✓ | ✓ | ✓ | PA |
| ... | ... | ... | ... | ER (any required field missing) |

All 12 combinations with at least one required field unfilled correctly resolve to "Show error"; the 2 fully-filled combinations resolve to "Publish the article."
