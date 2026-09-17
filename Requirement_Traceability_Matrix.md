# Requirement Traceability Matrix (RTM)

Maps each functional requirement to the test case(s) that validate it, and to
the automated coverage where one exists. Used to confirm complete test
coverage before sign-off (an SIT/UAT exit-criteria check).

| Req ID | Requirement                                                        | Test Case(s)        | Automated Coverage                                  |
|--------|--------------------------------------------------------------------|---------------------|----------------------------------------------------|
| REQ-01 | A bank manager can onboard a new client (customer)                 | TC_01, TC_02         | Cypress: `manager-client-onboarding.cy.js` (TC_01)   |
| REQ-02 | A bank manager can open an account for an existing client           | TC_03                | Cypress: `manager-client-onboarding.cy.js` (TC_02)   |
| REQ-03 | The client directory reflects all onboarded clients accurately      | TC_04                | Cypress: `manager-client-onboarding.cy.js` (TC_03)   |
| REQ-04 | A bank manager can remove a client record                           | TC_05                | Not automated (planned)                              |
| REQ-05 | A client can deposit funds into their account                       | TC_06                | Cypress: `customer-account-transactions.cy.js` (TC_04) |
| REQ-06 | A client can withdraw funds within their available balance          | TC_07                | Cypress: `customer-account-transactions.cy.js` (TC_06) |
| REQ-07 | The system rejects withdrawals exceeding the available balance      | TC_08                | Cypress: `customer-account-transactions.cy.js` (TC_05) |
| REQ-08 | Transaction history accurately reflects all credits and debits      | TC_09, TC_10, TC_11  | Cypress: `customer-account-transactions.cy.js` (TC_07) |
| REQ-09 | Account currency selected at opening is preserved and displayed     | TC_12                | Selenium: `test_customer_login_basic.py` (login/dashboard load) |

**Coverage summary:** 9/9 requirements have at least one manual test case;
7/9 have automated regression coverage. REQ-04 (delete client) is planned
for automation in a future iteration.
