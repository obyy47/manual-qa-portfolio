# Manual Testing Portfolio

Hi, I'm **Robby Adriansyah Fadillah**, an Information Technology graduate (Telkom University) looking for an entry-level **QA / Software Tester** role.

This repository shows how I plan, run, and report manual tests on two web applications.

| Project | What it is | Test cases | Test runs | Bugs found |
|---|---|---|---|---|
| [Seragam SD](./seragam-sd) | A school uniform ordering web app (PHP + MySQL) with parent and admin roles | 22 | 8 | 0 (all runs passed) |
| [SauceDemo](./saucedemo) | A public demo e-commerce site for testing practice | 48 | 13 | 12 |

## Tools

- **Qase**: test case management and test runs
- **Jira**: bug tracking
- **Browsers**: Chrome and Firefox

## How I test

- Positive, negative, boundary, and edge cases for each feature.
- Test types: Functional, Smoke, and Security.
- Test runs per feature, plus dedicated Smoke and Security runs.
- Bug reports with steps to reproduce, actual vs expected result, severity, priority, and screenshots.
- Failed test cases are linked to their Jira ticket (for example `Bug: SCRUM-5`).

## Where to start

1. [`saucedemo/bug-reports.md`](./saucedemo/bug-reports.md): the 12 bugs I found and reported
2. [`saucedemo/README.md`](./saucedemo/README.md): suites, test runs, and results
3. [`seragam-sd/README.md`](./seragam-sd/README.md): role-based tests (parent vs admin) and access control
4. [Related repositories](#related-repositories): automated UI, API, and performance testing portfolios built on top of these test cases

## Notes

- SauceDemo is a public practice site and its bugs are intentional. I used it to practice finding and reporting issues clearly.
- Seragam SD is a personal learning project that I used to practice designing tests for roles and access control.
- Test cases and screenshots are exported from Qase and Jira.

## Related repositories

| Repository | Category | What it covers |
|---|---|---|
| [postman-api-testing](https://github.com/obyy47/postman-api-testing) | API Testing | API tests for Reqres and Restful Booker: assertions, JSON Schema validation, and request chaining |
| [wdio-saucedemo-automation](https://github.com/obyy47/wdio-saucedemo-automation) | UI Automation (JS) | WebdriverIO E2E automation for SauceDemo using the Page Object pattern across Chrome and Firefox |
| [selenium-saucedemo-automation](https://github.com/obyy47/selenium-saucedemo-automation) | UI Automation (Python) | Selenium WebDriver + pytest E2E suite using Page Object Model, parallel runs, HTML report, and GitHub Actions CI |
| [k6-performance-testing](https://github.com/obyy47/k6-performance-testing) | Performance Testing | k6 load, stress, spike, and data-driven tests with custom metrics, HTML reports, and GitHub Actions CI |
| [jmeter-performance-testing](https://github.com/obyy47/jmeter-performance-testing) | Performance Testing | Apache JMeter load testing plans, thread group configurations, assertions, and HTML dashboard reports |

## Next

- Mobile test automation using **Appium**.

## Contact

- LinkedIn: https://www.linkedin.com/in/robbyadriansyahf/
- GitHub: https://github.com/obyy47
- Email: robbyadriansyah7@gmail.com