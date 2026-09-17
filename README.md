# Wealth Management / Portfolio QA — Test Case & Execution Documentation

Manual test planning, test case design, execution tracking, defect logging,
and requirement traceability for a client-onboarding / account-opening /
account-transactions module — demonstrating the SIT/UAT and test
documentation practices used in **wealth management and investment
operations QA**.

> Personal practice / portfolio project. Written against a public
> QA-training sandbox (the same [XYZ Bank demo](https://www.globalsqa.com/angularJs-protractor/BankingProject/#/login)
> used by the companion automation repos below) as a stand-in system, and
> **not** based on any employer's confidential systems, clients or data.

## Companion automation repos

- [`cypress-portfolio-automation`](https://github.com/tanzeelashaik02-cell/cypress-portfolio-automation) — Cypress + Page Object Model regression suite
- [`selenium-webdriver-basics`](https://github.com/tanzeelashaik02-cell/selenium-webdriver-basics) — basic Selenium WebDriver script

## Contents

| File                                    | Purpose                                                                 |
|------------------------------------------|--------------------------------------------------------------------------|
| `Test_Plan.md`                           | Scope, approach, environment, entry/exit criteria                       |
| `Test_Cases.csv`                         | 12 manual SIT/UAT-style test cases (positive & negative), execution status |
| `Requirement_Traceability_Matrix.md`     | Maps requirements → test cases → automated coverage                     |
| `Defect_Log_Template.csv`                | Defect tracking template, with illustrative example entries              |

## Skills demonstrated

Manual & functional testing · SIT/UAT execution · test case design ·
requirement & impact analysis · requirement traceability · defect
lifecycle management · data consistency checks · negative testing

## Notes

Test data (customers/accounts) was created directly through the sandbox UI
during execution, since the public demo exposes no API for seeding data —
mirroring the "test data preparation" activity described in the test plan.
The defect log entries are clearly marked as illustrative examples of the
tracking format, not real production defects.
