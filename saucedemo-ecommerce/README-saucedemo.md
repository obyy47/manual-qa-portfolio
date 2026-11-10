# SauceDemo: Manual Testing

Target site: https://www.saucedemo.com (a public demo store for testing practice).

## Test suites (48 test cases)

| Suite | Test cases |
|---|---|
| Login | 12 |
| Product List (sorting, product display) | 7 |
| Shopping Cart | 7 |
| Checkout | 14 |
| Logout | 7 |
| End-to-End | 1 |

**Types:** Functional (most), Smoke (4 core test cases), and Security (5 access-control and session tests).

## Approach

- Each test case is written once and **run with different accounts**: `standard_user` as the baseline, then `problem_user`, `error_user`, `visual_user`, and `performance_glitch_user`. A difference from `standard_user` points to a bug.
- `locked_out_user` is tested as a **negative** case: login must be rejected with an error message.
- Extra negative and edge cases: wrong or empty credentials, empty cart checkout, empty and whitespace-only checkout fields, direct URL access without login, and the browser Back button after logout.

## Test runs (13)

| # | Test run | Result |
|---|---|---|
| 1 | Login (Positive) | Passed |
| 2 | Product List & Sorting (Positive) | Failed |
| 3 | Shopping Cart (Positive) | Failed |
| 4 | Checkout (Positive) | Failed |
| 5 | Logout (Positive) | Failed |
| 6 | End-to-End (Positive) | Passed |
| 7 | Login (Negative) | Passed |
| 8 | Product List (Negative) | Passed |
| 9 | Shopping Cart (Negative) | Failed |
| 10 | Checkout (Negative) | Failed |
| 11 | Logout (Negative) | Passed |
| 12 | Smoke Testing Suite | Passed |
| 13 | Security & Access Control | Passed |

## Exported test runs

Selected runs, exported from Qase, are in [`test-runs/`](./test-runs):

| File | Why this run |
|---|---|
| `saucedemo-run02-product-list.csv` | Failed run: sorting and visual bugs |
| `saucedemo-run04-checkout-positive.csv` | Failed run: form and button bugs |
| `saucedemo-run06-end-to-end.csv` | One full user journey |
| `saucedemo-run10-checkout-negative.csv` | Failed run: validation gaps |
| `saucedemo-run12-smoke.csv` | Core flow check |
| `saucedemo-run13-security.csv` | Access control and session after logout |


## Bugs

12 bugs were reported in Jira: 2 Critical, 5 Major, 4 Normal, and 1 Minor. See [`bug-reports.md`](./bug-reports.md) for the full list with severity, priority, related test cases, and evidence.

## Files

- `test-cases.xlsx` / `test-cases.csv`: all test cases exported from Qase
- `test-runs/`: selected exported test runs
- `bug-reports.md`: summary of the 12 bugs
- `screenshots/qase/`: test suites, test runs, and sample test cases
- `screenshots/jira/`: ticket list and one full ticket
- `screenshots/bugs/SCRUM-5/` to `SCRUM-16/`: evidence for each bug
