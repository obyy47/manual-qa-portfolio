# SauceDemo: Bug Reports

12 bugs reported in Jira. Each ticket includes steps to reproduce, actual vs expected result, severity, priority, and screenshots.

> SauceDemo is a practice site and these issues are intentional. The goal here is to show clear and complete bug reporting.

| # | Jira ID | Summary | Account | Severity | Priority | Related test cases | Evidence |
|---|---|---|---|---|---|---|---|
| 1 | SCRUM-6 | Sorting has no effect except default A-Z | problem_user | Major | Medium | SWA-8 | `screenshots/bugs/SCRUM-6/bug-01.png` |
| 2 | SCRUM-7 | Sorting shows "Sorting is broken!" alert and fails | error_user | Major | Medium | SWA-10 | `screenshots/bugs/SCRUM-7/bug-01.png` |
| 3 | SCRUM-8 | Price sorting returns wrong order | visual_user | Major | Medium | SWA-11 | `screenshots/bugs/SCRUM-8/bug-03.png` |
| 4 | SCRUM-9 | Product images replaced with dog photos | problem_user, visual_user | Normal | Medium | SWA-8, SWA-11, SWA-21, SWA-26 | `screenshots/bugs/SCRUM-9/bug-01.png` |
| 5 | SCRUM-5 | "Add to cart" and "Remove" buttons unresponsive on the inventory page | problem_user, error_user | Critical | High | SWA-13, SWA-15 | `screenshots/bugs/SCRUM-5/bug-02.png` |
| 6 | SCRUM-10 | Entering Last Name overwrites First Name and blocks checkout | problem_user | Major | High | SWA-18 | `screenshots/bugs/SCRUM-10/bug-01.png` |
| 7 | SCRUM-11 | Last Name cannot be typed and validation is bypassed | error_user | Major | High | SWA-20 | `screenshots/bugs/SCRUM-11/bug-01.png` |
| 8 | SCRUM-12 | "Finish" button unresponsive on checkout overview | error_user | Critical | High | SWA-20 | `screenshots/bugs/SCRUM-12/bug-01.png` |
| 9 | SCRUM-13 | UI layout misaligned across pages (cart badge, hamburger menu, Checkout button, prices) | visual_user | Normal | Medium | SWA-11, SWA-16, SWA-21, SWA-26 | `screenshots/bugs/SCRUM-13/bug-03.png` |
| 10 | SCRUM-14 | About 5 second delay on login, sorting, Continue Shopping, and Back Home | performance_glitch_user | Minor | Low | SWA-4, SWA-9, SWA-14, SWA-19 | `screenshots/bugs/SCRUM-14/bug-01.txt` |
| 11 | SCRUM-15 | Checkout is allowed with an empty cart | standard_user | Normal | Medium | SWA-37 | `screenshots/bugs/SCRUM-15/bug-01.png` |
| 12 | SCRUM-16 | Whitespace-only values accepted in checkout fields | standard_user | Normal | Medium | SWA-44, SWA-45, SWA-46, SWA-47 | `screenshots/bugs/SCRUM-16/bug-07.png` |

## Summary by severity

| Severity | Count |
|---|---|
| Critical | 2 |
| Major | 5 |
| Normal | 4 |
| Minor | 1 |
| **Total** | **12** |

## Example: bug #5

**Summary:** "Add to cart" and "Remove" buttons are unresponsive on the inventory page (problem_user, error_user)

**Steps to reproduce**
1. Open https://www.saucedemo.com and log in as `problem_user` / `secret_sauce`.
2. Click "Add to cart" on "Sauce Labs Backpack", "Sauce Labs Bike Light", and "Sauce Labs Bolt T-Shirt".
3. Click "Remove" on the added items.
4. Repeat with `error_user`.

**Actual result:** Some "Add to cart" buttons do nothing (for example "Sauce Labs Bolt T-Shirt"). For items that were added, the "Remove" button on the inventory page cannot be clicked. The cart page shows 2 items instead of 3.

**Expected result:** All items are added, and "Remove" works on the inventory page.

**Comparison:** Works correctly with `standard_user`.

**Severity / Priority:** Critical / High
