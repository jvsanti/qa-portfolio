# OWASP Juice Shop — Checklist Execution

![env](https://img.shields.io/badge/ENV-Training_App-lightgrey?style=flat-square) `OWASP security-training platform (not production)`

Structured requirement-based checklists for Registration and Login, executed and tracked Pass/Fail. Registration: 10/10 executed, 8 passed, 2 failed. Login: 10/10 executed, 6 passed, 4 failed.

---

### `JS-REG-01` Password minimum length not enforced

![Critical](https://img.shields.io/badge/SEVERITY-CRITICAL-red?style=flat-square) `Priority: Critical`

**Steps to reproduce**
1. Go to the Registration form
2. Enter a password shorter than 8 characters
3. Submit

**Expected:** Form should reject passwords under 8 characters.

**Actual:** Short password is accepted with no error — the form does not enforce its own stated policy.

---

### `JS-REG-02` Password complexity not enforced

![Critical](https://img.shields.io/badge/SEVERITY-CRITICAL-red?style=flat-square) `Priority: Critical`

**Steps to reproduce**
1. Go to the Registration form
2. Enter a password with no uppercase, digit, or special character
3. Submit

**Expected:** Form should require uppercase, digit, and special character as stated in the password advice.

**Actual:** Weak password accepted without any complexity validation.

---

### `JS-LOGIN-01` 'Remember me' does not persist session

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Log in with 'Remember me' checked
2. Close and reopen the browser

**Expected:** User should remain logged in.

**Actual:** User is logged out — the option has no effect.

---

### `JS-LOGIN-02` Enter key does not submit login form

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Fill Email and Password
2. Press Enter instead of clicking the login button

**Expected:** Form submits and logs the user in.

**Actual:** Nothing happens — only clicking the button works.

---

### `JS-LOGIN-03` Login button not disabled by default

![Minor](https://img.shields.io/badge/SEVERITY-MINOR-blue?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. Open the login form before filling any field

**Expected:** Log in button should be disabled until required fields are filled.

**Actual:** Button is clickable by default, before any input.

---

### `JS-LOGIN-04` 'Forgot your password?' link non-functional

![Moderate](https://img.shields.io/badge/SEVERITY-MODERATE-yellow?style=flat-square) `Priority: Medium`

**Steps to reproduce**
1. On the login form, click 'Forgot your password?'

**Expected:** User is taken to a password-recovery flow.

**Actual:** Link does not work as expected.

---
