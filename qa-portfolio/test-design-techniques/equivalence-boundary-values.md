# Test Design: Equivalence Partitioning & Boundary Value Analysis

Applied to password field requirements: 4-16 characters, ≥1 uppercase, ≥1 special character.

## Equivalence Classes

| Rule | Class | Example | Expected |
|---|---|---|---|
| Min length 4 | Below minimum | `abc` | Error: min 4 characters |
| Min length 4 | Valid | `abcd` | Accepted |
| Max length 16 | Within range | `Abcdef1!` | Accepted |
| Max length 16 | Above maximum | `Abcdefghij123456!` | Error: max 16 characters |
| Uppercase required | Missing | `abcdef1!` | Error: needs uppercase |
| Uppercase required | Present | `Abcdef1!` | Accepted |
| Special char required | Missing | `Abcdef12` | Error: needs special char |
| Special char required | Present | `Abcdef1!` | Accepted |

## Boundary Values

| Rule | Boundary | Example | Expected |
|---|---|---|---|
| Min length 4 | 3 (below) | `Ab1!` | Error |
| Min length 4 | 4 (min) | `Abc1!` | Accepted |
| Min length 4 | 5 (above) | `Abcd1!` | Accepted |
| Max length 16 | 15 (below) | `Abcdefghijklm1!` | Accepted |
| Max length 16 | 16 (max) | `Abcdefghijklmn1!` | Accepted |
| Max length 16 | 17 (above) | `Abcdefghijklmno1!` | Error |
