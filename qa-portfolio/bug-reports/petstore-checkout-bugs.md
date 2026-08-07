# PetStore — Checkout Flow: Bugs Found

**PS-0001.** It is possible to proceed to checkout with an out-of-stock product ('Adult Male Amazon Parrot', marked In Stock? = false) — the Proceed to Checkout button stays enabled.

**PS-0002.** The Quantity field accepts values with no upper limit — entering 999 for one item resulted in a Total Cost of $193,499,806.50 with no validation error or maximum-quantity restriction.

**PS-0003.** The Card Number field accepts letters and any character format without validation ('999 9999 9999 adasdasda' was accepted; Continue button stayed enabled).

**PS-0004.** Same Card Number validation issue reproduced a second time during checkout.

**PS-0005.** HTTP 500 error page displayed when confirming an order. Stack trace shows `DataIntegrityViolationException` — "numeric value out of range" on `ORDERS.TOTALPRICE` — consistent with the unlimited-quantity bug (PS-0002): the order total likely exceeds the database column's numeric capacity.
