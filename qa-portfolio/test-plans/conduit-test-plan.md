# Conduit — Test Plan

## Introduction

"Conduit" is an open-source application used to train software development and testing skills. Main functionality: registration/sign-in, posting articles, reading articles, liking articles, commenting, and following users.

This Test Plan defines the scope, approach, resources, and schedule of all testing activities for the Conduit website.

## 1. Test Strategy

### 1.1 Testing Scope

**1.1.1 Features to be tested**

| Module | Login type | Description |
|---|---|---|
| Conduit logo | Logged in / out | Navigates to Home from anywhere |
| Home | Logged in / out | 'Your Feed' and 'Global Feed' tabs with article previews and popular tags |
| Sign in | Logged out | Email + Password form |
| Sign up | Logged out | Username + Email + Password form |
| Your Feed tab | Logged in | Articles from followed users, newest first |
| Global Feed tab | Logged in / out | All articles, 10 per page |
| Popular tags | Logged in / out | Filter Global Feed by tag |
| New Article page | Logged in | Publish article form (title, description, Markdown body, tags) |
| Settings page | Logged in | Update profile (picture, username, bio, email, password) |
| User page | Logged in / out | Profile info, My Posts / Favorited Posts |
| Article page | Logged in / out | Full article, edit/delete (author only), comments |

**1.1.2 Out of scope:** Website Security, Website Performance, Website API testing, Test Automation.

**1.2 Test types:** System testing — exploratory, smoke (each new build), functional, GUI, compatibility (Windows/macOS browsers only).

**1.3 Risks and Issues**

| Risk | Mitigation |
|---|---|
| Team lacks required testing skills | Access to documentation and example artifacts; pair with mentor on first cycle |
| Not enough time to test all browsers/OS | Prioritize by usage share; document untested combinations as known limitation |
| Not enough time to execute all scenarios | Prioritize by risk/impact (P0/P1 first); track daily progress |
| Team member unavailable | Cross-train on modules; keep test cases in shared documents |

**1.4 Test Logistics:** QA team executes assigned modules, logs bugs, reports daily progress to mentor/lead. Testing starts once test cases are reviewed, the environment is stable, and test data is prepared.

## 2. Test Objective

Verify functionality and API of the Conduit app, focused on publishing articles and sharing information between members: authorization, posting, following, favoriting, likes, comments.

## 3. Test Criteria

**3.1 Suspension:** 10% of P0/P1 failed → suspend until fixed. 30% of P2/P3 failed → suspend until fixed.

**3.2 Exit criteria:** Execution rate ≥95% · Pass rate 100% (P0/P1) · Pass rate ≥80% (P2/P3) · All artifacts collected · No open Critical/Major bugs or High-priority bugs · Known-bug list agreed with dev/PM.

## 4. Resource Planning

**System:** Chrome + Firefox (latest) · stable broadband (10 Mbps+) · Windows 10/11 or macOS, 1366x768+.

**Human:** QA members (design/execute test cases, log bugs, verify fixes, report progress) · Mentors (review, prioritize, unblock, stakeholder comms).

## 5. Test Environment

Production environment; local runs via Docker for DB work.

## 6. Schedule & Estimation

| Task | Members | Effort |
|---|---|---|
| Create Test Plan | QA | 3h |
| Decomposition, decision table, state diagram | QA | 4h |
| Create test cases | QA | 8h |
| Review test cases | Mentors | 2h |
| Test case execution | QA | 12h |
| Bug reports | QA | 3h |
| Test report | QA | 2h |

Spread across 3 sprints (planning → design/execution → execution/reporting).

## 7. Test Deliverables

- Before: Test Plan, Test Cases
- During: Bug Reports, execution checklist (Pass/Fail)
- After: Test Report (summary + bug stats), known issues list
