# PetStore — Shopping Cart: STLC (Test Design + Execution)

Full test cycle: checklist design → execution → bug reporting → statistics. Run date: 03/08/2026.

## Execution Statistics

| Total | Executed | Execution Rate | Passed | Pass Rate | Failed |
|---|---|---|---|---|---|
| 30 | 30 | 100% | 22 | 73.3% | 8 |

## Bug Statistics

| Severity | Count | % |
|---|---|---|
| Critical | 0 | 0% |
| Major | 1 | 12.5% |
| Moderate | 5 | 62.5% |
| Minor | 2 | 25% |
| **Total** | **8** | **100%** |

## Checklist & Results

| # | Checklist item | Priority | Result | Bug ID |
|---|---|---|---|---|
| 1 | The Cart is accessible from any page in the app | High | Passed | |
| 2 | The Cart icon displays a tooltip with the text 'Cart' on hover | Medium | Failed | PS-001 |
| 3 | The product table displays all required columns (Item ID, Product ID, Name, Description, In Stock?, Quantity, List Price, Total Cost) | High | Failed | PS-002 |
| 4 | Last row displays 'Sub Total' + 'Update Cart' button | High | Passed | |
| 5 | Cart contains no products by default | Medium | Passed | |
| 6 | Empty Cart displays 'Your cart is empty.' | Medium | Passed | |
| 7 | 'Proceed to Checkout' shown when ≥1 product in cart | High | Passed | |
| 8 | 'Proceed to Checkout' hidden when cart empty | Medium | Passed | |
| 9 | 'Proceed to Checkout' redirects logged-in user to Checkout | Critical | Passed | |
| 10 | 'Proceed to Checkout' redirects logged-out user to Login | Critical | Passed | |
| 11 | 'Return to Main Menu' navigates away from Cart | Medium | Passed | |
| 12 | Product can be added to Cart from PDP | Critical | Passed | |
| 13 | Product can be added to Cart from product list | Critical | Passed | |
| 14 | Adding a product shows correct badge count on Cart icon | High | Failed | PS-003 |
| 15 | 'Item ID' value is a clickable link | Medium | Passed | |
| 16 | 'Name' value is a clickable link | Medium | Skipped | — (field doesn't exist in Cart table) |
| 17 | 'Quantity' field rejects non-numeric values | Critical | Passed | |
| 18 | Users cannot add more than 5 items of the same product | Critical | Failed | PS-004 |
| 19 | Exactly 5 items accepted without validation message (boundary) | High | Passed | |
| 20 | 6 items triggers 'can't buy more than 5 items' message (boundary) | High | Failed | PS-005 |
| 21 | Quantity validation triggers on Enter | High | Passed | |
| 22 | Quantity validation triggers on 'Update Cart' click | High | Passed | |
| 23 | Max-quantity error message displayed when quantity > 5 | Critical | Failed | PS-006 |
| 24 | Out-of-stock quantity error message displayed | Critical | Failed | PS-007 |
| 25 | Product can be removed via 'Remove' button | Critical | Passed | |
| 26 | Quantity 0 + 'Update Cart' removes the product | High | Passed | |
| 27 | Out-of-stock product cannot be added to Cart | Critical | Failed | PS-008 |
| 28 | Product added by logged-in user shows in all their active sessions | High | Passed | |
| 29 | Cart empties for the session after logout | High | Passed | |
| 30 | Removing a product removes it across all active sessions | High | Passed | |

## Bugs Found

**PS-001 — Minor.** Cart icon does not show a tooltip on hover.
Steps: go to Cart page → hover the Cart icon. Expected: tooltip 'Cart'. Actual: no tooltip.

**PS-002 — Moderate.** Product table in the Cart is missing the Name column (name shown in Description column instead).

**PS-003 — Moderate.** Adding a product does not update the badge count on the Cart icon.
Repro: open a product page → Add to Cart → check Cart icon. No badge is displayed.

**PS-004 — Moderate.** System allows adding more than 5 units of the same product (accepted 99, no error, Total Cost updates normally).

**PS-005 — Moderate.** Entering 6+ in Quantity does not trigger the "can't buy more than 5 items" validation message.

**PS-006 — Minor.** Max-quantity error message text never displays even when the limit is exceeded.

**PS-007 — Moderate.** No "insufficient stock" message shown when requested quantity exceeds available stock; quantity is accepted anyway.

**PS-008 — Major.** A product marked `In Stock? = false` can still be added to the Cart in any quantity, with no blocking message.
