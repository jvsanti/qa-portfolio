<div align="center">

# QA Portfolio

![Test Cases](https://img.shields.io/badge/Test_Cases-71-blue?style=flat-square)
![Bugs Found](https://img.shields.io/badge/Bugs_Found-39-orange?style=flat-square)
![Sites Tested](https://img.shields.io/badge/Sites_Tested-13-brightgreen?style=flat-square)
![Pass Rate](https://img.shields.io/badge/STLC_Pass_Rate-73%25-yellow?style=flat-square)

</div>

Practical work from my QA Engineering certification (Mate Academy): test planning, test case design, execution, and bug reporting. Some of it on training apps (Conduit, PetStore, OWASP Juice Shop), some on real live production sites (AIESEC, Domino's Brazil).

Before software QA, I spent 6+ years as a Quality Analyst in automotive manufacturing (IATF 16949 / ISO 9001), as an on-site resident for an OEM client (Stellantis, Nissan). The root-cause logic I use there — 8D, Pareto, Ishikawa — is the same one I applied here to investigate bugs. In that role I also built ARGOSYS, a full-stack quality-inspection system used in the field at WHB/Stellantis.


## Contents

- [`test-plans/`](./test-plans) — full STLC Test Plan for the Conduit app
- [`test-cases/`](./test-cases) — 71 formal test cases (STLC cycle, user stories, login flows)
- [`bug-reports/`](./bug-reports) — 34+ real bugs across 13 sites/apps (index below)
- [`test-design-techniques/`](./test-design-techniques) — equivalence partitioning, boundary values, decision table, pairwise
- [`api-testing/`](./api-testing) — Postman API tests with scripted assertions

## Bug reports index

| Site | Environment | Bugs found | Highest severity |
|---|---|---|---|
| [Domino's Brazil](./bug-reports/dominos-bugs.md) | Real production | 2 | Major |
| [AIESEC](./bug-reports/aiesec-bugs.md) | Real production | 2 | Minor |
| [Bern.com](./bug-reports/bern-bugs.md) | Real production | 2 | Major |
| [Global Lives Project](./bug-reports/globallives-bugs.md) | Real production | 2 | Moderate |
| [Stellarium](./bug-reports/stellarium-bugs.md) | Real production | 2 | Minor |
| [Cinks Labs](./bug-reports/cinks-labs-bugs.md) | Real production | 2 | Minor |
| [EnergyTelecom](./bug-reports/energytelecom-bugs.md) | Real production | 3 | Moderate |
| [Lumos](./bug-reports/lumos-bugs.md) | Real production | 1 | Moderate |
| [OWASP Juice Shop](./bug-reports/juice-shop-checklists.md) | Security training | 6 | Critical |
| [Sweet Shop](./bug-reports/sweetshop-bugs.md) | Training app | 2 | Moderate |
| [Conduit (RealWorld)](./bug-reports/conduit-realworld-bugs.md) | Training app | 3 | Major |
| [PetStore checkout](./bug-reports/petstore-checkout-bugs.md) | Training app | 4 | Critical |
| [PetStore cart (STLC)](./test-cases/petstore-cart-stlc.md) | Training app | 8 | Major |

Two worth reading in full: the **Domino's Brazil** checkout bug (real production site, cart with no quantity cap breaks the order total) and the **OWASP Juice Shop** password-policy findings (the registration form doesn't enforce the complexity rules it advertises).

## Stack

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![TestRail](https://img.shields.io/badge/TestRail-65C179?style=flat-square&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

## Contact

 · [LinkedIn](https://linkedin.com/in/jvsanti)
