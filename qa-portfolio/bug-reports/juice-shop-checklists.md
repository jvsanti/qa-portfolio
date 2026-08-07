# OWASP Juice Shop — Checklist Execution (Registration + Login)

Structured requirement-based checklists, executed and tracked with Pass/Fail per item.

## Registration Form — 10/10 executed, 8 Passed, 2 Failed

| # | Requirement | Priority | Result |
|---|---|---|---|
| 1 | Email field accepts only a valid email address | High | Passed |
| 2 | Email field rejects an already-registered address | High | Passed |
| 3 | Password must be ≥8 characters | Critical | **Failed** |
| 4 | Password must contain lowercase, uppercase, digit, and special symbol | Critical | **Failed** |
| 5 | Repeat Password must match Password | Critical | Passed |
| 6 | "Show password advice" toggle disabled by default | High | Passed |
| 7 | "Show password advice" displays all requirements when activated | High | Passed |
| 8 | Security Question dropdown displays options | High | Passed |
| 9 | Email/Password/Repeat/Security Q&A are mandatory | Critical | Passed |
| 10 | "Already a customer?" links to login | High | Passed |

**Finding of note:** the two failed checks (#3, #4) mean the app's actual password policy does not enforce its own stated complexity requirements — a real gap with security relevance, not just cosmetic.

## Login Form — 10/10 executed, 6 Passed, 4 Failed

| # | Requirement | Priority | Result |
|---|---|---|---|
| 1 | Email and Password fields present | Critical | Passed |
| 2 | Login succeeds with valid registered credentials | Critical | Passed |
| 3 | "Remember me" keeps the user logged in | Critical | **Failed** |
| 4 | Login works via Enter key (not just button click) | High | **Failed** |
| 5 | Log in button disabled by default (before fields filled) | High | **Failed** |
| 6 | Invalid credentials are rejected | High | Passed |
| 7 | "Invalid email or password" message shown on failed login | High | Passed |
| 8 | "Not yet a customer?" links to Registration | High | Passed |
| 9 | "Forgot your password?" link works | High | **Failed** |
| 10 | Password becomes visible via "Show password" | High | Passed |
