# ParaBank — Test Scenarios

This document summarizes the 45 existing manual test cases for the ParaBank portfolio across seven functional areas. Each scenario maps to the test case with the same numeric ID and preserves its assigned priority. Detailed steps, test data, and execution results belong in the corresponding test cases.

**Priority:** Critical — core banking or authentication checks; High — important workflows and validation; Medium — supporting functionality and supplementary checks. Priorities indicate execution order, not defect severity.

## 01 — Login

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-001 | TC-001 | Verify that valid credentials authenticate the user and display Accounts Overview. | Critical |
| TS-002 | TC-002 | Verify that login with an invalid password is rejected with an appropriate error message. | High |
| TS-003 | TC-003 | Verify that login with an invalid username is rejected with an appropriate error message. | High |
| TS-004 | TC-004 | Verify that login with an empty username is prevented with a validation or error message. | High |
| TS-005 | TC-005 | Verify that login with an empty password is prevented with a validation or error message. | High |
| TS-006 | TC-006 | Verify that login with both credentials empty is prevented with validation or error messages. | High |
| TS-007 | TC-007 | Verify that the SQL injection input defined in TC-007 does not authenticate the user. | Medium |
| TS-008 | TC-008 | Verify that logout after successful login ends authenticated access, including when using the browser Back button. | High |

## 02 — Registration

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-009 | TC-009 | Verify that valid registration data and a unique username create a user account and display confirmation. | Critical |
| TS-010 | TC-010 | Verify that registration with all required fields empty is prevented with validation messages. | High |
| TS-011 | TC-011 | Verify that registration with mismatched passwords is prevented with a validation message. | High |
| TS-012 | TC-012 | Verify that registration with an existing username is rejected with an appropriate message. | High |
| TS-013 | TC-013 | Verify that registration with an empty username is prevented with a required-field message. | High |
| TS-014 | TC-014 | Verify that registration with empty Password and Confirm fields is prevented with validation messages. | High |

## 03 — Accounts

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-015 | TC-015 | Verify that Accounts Overview displays the authenticated user's accounts, account numbers, and balances. | High |
| TS-016 | TC-016 | Verify that account details display the correct account number, type, balance, and available balance. | High |
| TS-017 | TC-017 | Verify that transaction history lists the transactions for the selected account. | High |
| TS-018 | TC-018 | Verify that selecting a transaction displays its corresponding details. | Medium |
| TS-019 | TC-019 | Verify that filtering by activity period displays only transactions matching the selected period. | Medium |
| TS-020 | TC-020 | Verify that filtering by transaction type displays only transactions matching the selected type. | Medium |

## 04 — Fund Transfer

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-021 | TC-021 | Verify that a valid transfer between different accounts succeeds and displays the amount and account details. | Critical |
| TS-022 | TC-022 | Verify that a transfer with an empty amount is prevented with a validation or error message. | High |
| TS-023 | TC-023 | Verify that a transfer with a zero amount is prevented with a validation or error message. | High |
| TS-024 | TC-024 | Verify that a transfer with a negative amount is rejected without moving funds. | Critical |
| TS-025 | TC-025 | Verify that a transfer with a nonnumeric amount is prevented with a validation or error message. | High |
| TS-026 | TC-026 | Verify that a valid decimal amount is transferred accurately between the selected accounts. | High |
| TS-027 | TC-027 | Verify that a transfer using the same source and destination account is prevented or rejected. | High |
| TS-028 | TC-028 | Verify that a transfer exceeding the available balance is rejected without reducing the source balance, subject to the confirmed overdraft rules. | Critical |
| TS-029 | TC-029 | Verify that a successful transfer decreases the source balance and increases the destination balance by the transferred amount. | Critical |
| TS-030 | TC-030 | Verify that a successful transfer appears in both accounts' transaction histories with the correct amount and details. | High |

## 05 — Bill Payment

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-031 | TC-031 | Verify that a bill payment with valid data succeeds and displays confirmation with payment details. | Critical |
| TS-032 | TC-032 | Verify that bill payment with all required fields empty is prevented with validation messages. | High |
| TS-033 | TC-033 | Verify that bill payment with mismatched account numbers is prevented with a validation message. | High |
| TS-034 | TC-034 | Verify that bill payment with a zero amount is prevented with a validation or error message. | High |
| TS-035 | TC-035 | Verify that bill payment with a negative amount is rejected without deducting funds. | Critical |
| TS-036 | TC-036 | Verify that bill payment with a nonnumeric amount is prevented with a validation or error message. | High |

## 06 — Profile & Password

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-037 | TC-037 | Verify that valid contact information updates are saved and displayed after refreshing or reopening the profile. | Medium |
| TS-038 | TC-038 | Verify that profile updates with required fields empty are prevented with validation messages. | High |
| TS-039 | TC-039 | Verify that a valid password change allows login with the new password, where password changes are supported. | Critical |
| TS-040 | TC-040 | Verify that a password change with mismatched passwords is prevented with a validation message, where password changes are supported. | High |
| TS-041 | TC-041 | Verify that updated profile information persists after logout and subsequent login. | Medium |

## 07 — Logout & Session

| Scenario ID | Test Case | Scenario | Priority |
|---|---|---|---|
| TS-042 | TC-042 | Verify that logout ends the session and displays the login page. | High |
| TS-043 | TC-043 | Verify that using the browser Back button after logout does not restore access to protected functionality. | Critical |
| TS-044 | TC-044 | Verify that opening a protected page by direct URL after logout requires authentication. | Critical |
| TS-045 | TC-045 | Verify that the session remains active while navigating between protected application pages. | High |

## Coverage Summary

| Section | Scenario Range | Test Case Range | Count |
|---|---|---|---:|
| Login | TS-001–TS-008 | TC-001–TC-008 | 8 |
| Registration | TS-009–TS-014 | TC-009–TC-014 | 6 |
| Accounts | TS-015–TS-020 | TC-015–TC-020 | 6 |
| Fund Transfer | TS-021–TS-030 | TC-021–TC-030 | 10 |
| Bill Payment | TS-031–TS-036 | TC-031–TC-036 | 6 |
| Profile & Password | TS-037–TS-041 | TC-037–TC-041 | 5 |
| Logout & Session | TS-042–TS-045 | TC-042–TC-045 | 4 |
| **Total** | **TS-001–TS-045** | **TC-001–TC-045** | **45** |

Coverage includes successful workflows, required-field validation, invalid inputs, monetary values, transaction filtering, data persistence, and session access checks. This is coverage of the existing test suite, not a claim of complete application coverage or successful execution.

## Scope Notes

- TS-008 intentionally retains the existing login-to-logout check, which overlaps with TS-042 and TS-043, to preserve traceability to all 45 test cases.
- TS-039 and TS-040 retain the existing password-change cases. Confirm that the tested build provides this feature before execution; if unavailable, record the scope limitation instead of assuming that password fields exist on Update Contact Info.
- Confirm the applicable business rules for zero amounts, same-account transfers, and overdrafts before classifying unexpected behavior as a defect.
- For post-logout checks, distinguish a cached page from renewed authenticated access by attempting to access protected functionality.
