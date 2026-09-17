# Test Plan — Client Portfolio & Account Management Module

**Project:** Wealth Management / Investment Operations QA Practice Portfolio
**Module under test:** Client onboarding, account opening, and account
transaction processing (public demo sandbox used as the system under test —
see note below)
**Prepared by:** Tanzeela Shaik, QA / Test Analyst

> This documentation set is a personal practice / portfolio project that
> demonstrates test planning, test case design and execution, and defect
> lifecycle management skills used in wealth management and investment
> operations QA roles. It is written against a public QA-training sandbox
> (the "XYZ Bank" demo) as a stand-in system, and is **not** based on any
> employer's confidential systems, clients, or data.

## 1. Objective

Validate the core client-account lifecycle end to end:

- Client onboarding (Add Customer)
- Account opening (portfolio/cash account creation)
- Account transaction processing (deposits, withdrawals)
- Transaction history / data consistency

## 2. Scope

### In scope
- Functional testing of client onboarding and account opening
- Functional and negative testing of deposit/withdrawal transactions
- Data consistency checks between the client directory and account records
- Transaction history accuracy (credit/debit entries, running balance)

### Out of scope
- Performance/load testing
- Security testing
- Backend database validation (no direct DB access to the public sandbox)

## 3. Test Approach

- **Manual test case design and execution** for SIT/UAT-style functional
  coverage (see `Test_Cases.md`)
- **UI automation** (Cypress, Page Object Model) for regression coverage
  of the same scenarios — see the companion
  [`cypress-portfolio-automation`](https://github.com/tanzeelashaik02-cell/cypress-portfolio-automation)
  repo
- **Basic Selenium WebDriver** script for a subset of the login flow — see
  [`selenium-webdriver-basics`](https://github.com/tanzeelashaik02-cell/selenium-webdriver-basics)
- **Requirement traceability** maintained throughout (see
  `Requirement_Traceability_Matrix.md`)
- **Defect logging** for any discrepancy found during execution (see
  `Defect_Log_Template.csv`)

## 4. Test Environment

| Item              | Detail                                                                 |
|-------------------|-------------------------------------------------------------------------|
| Application       | Public QA-training banking sandbox (stand-in for a client/account system)|
| URL               | https://www.globalsqa.com/angularJs-protractor/BankingProject           |
| Browsers          | Chrome (primary)                                                        |
| Test data         | Created dynamically per test run (no reset available on the public sandbox — see Notes) |

## 5. Entry / Exit Criteria

**Entry criteria**
- Test cases reviewed and approved
- Test environment (sandbox URL) accessible

**Exit criteria**
- All planned test cases executed
- No open Critical/High severity defects
- Requirement Traceability Matrix fully mapped

## 6. Roles & Responsibilities

| Role         | Responsibility                                          |
|--------------|-----------------------------------------------------------|
| QA / Test Analyst | Test case design, execution, defect logging, RTM upkeep |

## 7. Risks & Notes

- The system under test is a **shared public sandbox** with no data reset
  or isolated test environment, so test data (customers/accounts) persists
  across runs. In a real SIT/UAT environment this would be mitigated with a
  dedicated test environment and a test data setup/teardown process.
- No API layer is exposed for direct data seeding, so all test data setup
  is done through the UI.
