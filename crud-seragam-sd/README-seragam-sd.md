# Seragam SD: Manual Testing

## About the application

A web application for ordering school uniforms (PHP + MySQL) with two roles:

- **Parent:** registers, logs in, manages children's data, creates orders, and edits or cancels an order while it is still awaiting payment.
- **Admin:** logs in, sees all orders from all parents, and moves each order through the statuses: awaiting payment, paid, processed, completed.

Rules I tested:
- A parent can only access their own data.
- Admin pages are blocked for parents and for users who are not logged in.
- The order total is calculated by the server.

## Test suites (22 test cases)

| Suite | Test cases |
|---|---|
| Authentication & Registration | 7 |
| User Order Flow | 2 |
| Child Data Management | 4 |
| Order Management | 5 |
| Admin Order Approval | 4 |

## Test runs (8)

| # | Test run | Result |
|---|---|---|
| 1 | Authentication & Registration | Passed |
| 2 | Logout Admin & User | Passed |
| 3 | User Order Flow | Passed |
| 4 | Edit & Delete child data | Passed |
| 5 | Edit & Batalkan Orders | Passed |
| 6 | Negative Cases Execution | Passed |
| 7 | Admin Order Approval Execution | Passed |
| 8 | Smoke Test | Passed |

All runs passed, so no bugs were reported for this application.

## Exported test runs

Selected runs, exported from Qase, are in [`test-runs/`](./test-runs):

| File | Why this run |
|---|---|
| `seragam-run06-negative.csv` | Invalid input and unauthorized access |
| `seragam-run08-smoke.csv` | Quick check of the core features |
| `seragam-run07-admin-approval.csv` | Admin role and order status workflow |


## What I focused on

- Positive and negative paths for registration and login
- Role-based access (parent vs admin) and ownership of data
- Order rules: edit or cancel only while awaiting payment, and the status workflow for admin
- Input validation (empty fields and invalid values)

## Files

- `test-cases.xlsx` / `test-cases.csv`: all test cases exported from Qase
- `test-runs/`: selected exported test runs
- `screenshots/qase`: test suites, test run list, and sample test cases from Qase
