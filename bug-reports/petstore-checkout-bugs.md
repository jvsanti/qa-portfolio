# PetStore — Checkout Flow: Bugs Found

![env](https://img.shields.io/badge/ENV-Training_App-lightgrey?style=flat-square) `jpetstore.mate.academy (training app)`

---

### `PS-CO-01` Out-of-stock product can be checked out

![Major](https://img.shields.io/badge/SEVERITY-MAJOR-orange?style=flat-square) `Priority: High`

**Steps to reproduce**
1. Add an out-of-stock product ('Adult Male Amazon Parrot', In Stock? = false) to the cart
2. Go to checkout

**Expected:** Checkout should be blocked for out-of-stock items.

**Actual:** Proceed to Checkout button stays enabled and checkout proceeds normally.

---

### `PS-CO-02` Quantity field has no upper limit

![Major](https://img.shields.io/badge/SEVERITY-MAJOR-orange?style=flat-square) `Priority: High`

**Steps to reproduce**
1. Add a product to the cart
2. Enter 999 in the Quantity field

**Expected:** A reasonable maximum should be enforced.

**Actual:** Value accepted with no validation — Total Cost becomes $193,499,806.50.

---

### `PS-CO-03` Card Number field accepts any characters

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Reach the payment step
2. Enter '999 9999 9999 adasdasda' in the Card Number field

**Expected:** Field should validate card number format.

**Actual:** Value is accepted; Continue button stays enabled.

---

### `PS-CO-04` HTTP 500 on order confirmation

![Critical](https://img.shields.io/badge/SEVERITY-CRITICAL-red?style=flat-square) `Priority: Critical`

**Steps to reproduce**
1. Trigger the unlimited-quantity bug (PS-CO-02)
2. Confirm the order

**Expected:** Order should be confirmed normally, or a clear user-facing error shown.

**Actual:** Server returns HTTP 500 (DataIntegrityViolationException — numeric value out of range on ORDERS.TOTALPRICE), consistent with the order total exceeding the database column's numeric capacity.

---
