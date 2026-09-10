# ParaBank | Test Scenarios

> **Manual Testing Portfolio**  
> 45 scenarios · 7 functional areas · TestRail traceability

I am creating this portfolio by manually testing the ParaBank demo banking application to demonstrate my test design and documentation skills.

This scenario index uses the exact test case titles, IDs, and priorities from my TestRail export. Scenario IDs provide a separate reference for this document.

## Contents

- [Login](#login)
- [Registration](#registration)
- [Accounts](#accounts)
- [Fund Transfer](#fund-transfer)
- [Bill Payment](#bill-payment)
- [Profile & Password](#profile-password)
- [Logout & Session](#logout-session)
- [Coverage Summary](#coverage-summary)
- [Scope Notes](#scope-notes)

### Priority Guide

**Critical** — highest execution priority · **High** — important workflows and validation · **Medium** — supporting checks

*Priorities match TestRail and do not represent defect severity. Execution results are recorded separately.*

---

<a id="login"></a>

## 01 · Login

**8 scenarios** · TS-001–TS-008

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-001** | `C46` | Login with valid credentials | **Critical** |
| **TS-002** | `C47` | Login with invalid password | High |
| **TS-003** | `C48` | Login with invalid username | High |
| **TS-004** | `C49` | Login with empty username | High |
| **TS-005** | `C50` | Login with empty password | High |
| **TS-006** | `C90` | Login with empty username and password | Medium |
| **TS-007** | `C51` | Login with SQL injection attempt | Medium |
| **TS-008** | `C52` | Verify successful logout after login | High |

---

<a id="registration"></a>

## 02 · Registration

**6 scenarios** · TS-009–TS-014

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-009** | `C53` | Register a new user with valid data | **Critical** |
| **TS-010** | `C54` | Registration with all required fields empty | High |
| **TS-011** | `C55` | Registration with mismatched passwords | High |
| **TS-012** | `C56` | Registration with an existing username | High |
| **TS-013** | `C57` | Registration with empty username | High |
| **TS-014** | `C58` | Registration with empty password | High |

---

<a id="accounts"></a>

## 03 · Accounts

**6 scenarios** · TS-015–TS-020

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-015** | `C59` | View Accounts Overview after successful login | High |
| **TS-016** | `C60` | View account details | High |
| **TS-017** | `C61` | View transaction history for an account | High |
| **TS-018** | `C62` | View transaction details | Medium |
| **TS-019** | `C63` | Filter transactions by activity period | Medium |
| **TS-020** | `C64` | Filter transactions by transaction type | Medium |

---

<a id="fund-transfer"></a>

## 04 · Fund Transfer

**10 scenarios** · TS-021–TS-030

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-021** | `C65` | Transfer funds between accounts with valid data | **Critical** |
| **TS-022** | `C66` | Transfer funds with empty amount | High |
| **TS-023** | `C67` | Transfer funds with zero amount | High |
| **TS-024** | `C68` | Transfer funds with negative amount | **Critical** |
| **TS-025** | `C69` | Transfer funds with invalid amount format | High |
| **TS-026** | `C70` | Transfer funds with valid decimal amount | High |
| **TS-027** | `C71` | Transfer funds using the same source and destination account | High |
| **TS-028** | `C72` | Transfer amount greater than available balance | **Critical** |
| **TS-029** | `C73` | Verify account balances after successful fund transfer | **Critical** |
| **TS-030** | `C74` | Verify transaction history after successful fund transfer | High |

---

<a id="bill-payment"></a>

## 05 · Bill Payment

**6 scenarios** · TS-031–TS-036

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-031** | `C75` | Pay a bill with valid data | **Critical** |
| **TS-032** | `C76` | Bill payment with all required fields empty | High |
| **TS-033** | `C77` | Bill payment with mismatched account numbers | High |
| **TS-034** | `C78` | Bill payment with zero amount | High |
| **TS-035** | `C79` | Bill payment with negative amount | **Critical** |
| **TS-036** | `C80` | Bill payment with invalid amount format | High |

---

<a id="profile-password"></a>

## 06 · Profile & Password

**5 scenarios** · TS-037–TS-041

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-037** | `C81` | Update profile information with valid data | Medium |
| **TS-038** | `C82` | Update profile with required fields empty | High |
| **TS-039** | `C83` | Change password with valid data | **Critical** |
| **TS-040** | `C84` | Change password with mismatched passwords | High |
| **TS-041** | `C85` | Verify updated profile data persists after re-login | Medium |

---

<a id="logout-session"></a>

## 07 · Logout & Session

**4 scenarios** · TS-042–TS-045

| Scenario ID | TestRail ID | Test Title | Priority |
| :---: | :---: | :--- | :---: |
| **TS-042** | `C86` | Successful logout | High |
| **TS-043** | `C87` | Access protected page after logout | **Critical** |
| **TS-044** | `C88` | Access protected page using direct URL after logout | **Critical** |
| **TS-045** | `C89` | Verify session remains active during authenticated navigation | High |

---

## Coverage Summary

| Functional Area | Scenarios | TestRail IDs |
| :--- | ---: | :--- |
| [Login](#login) | 8 | C46–C52, C90 |
| [Registration](#registration) | 6 | C53–C58 |
| [Accounts](#accounts) | 6 | C59–C64 |
| [Fund Transfer](#fund-transfer) | 10 | C65–C74 |
| [Bill Payment](#bill-payment) | 6 | C75–C80 |
| [Profile & Password](#profile-password) | 5 | C81–C85 |
| [Logout & Session](#logout-session) | 4 | C86–C89 |
| **Total** | **45** | **C46–C90** |

**Priority distribution:** 11 Critical · 27 High · 7 Medium

Coverage includes successful workflows, required-field validation, invalid inputs, monetary values, transaction filtering, data persistence, and session access checks.

## Scope Notes

- **Traceability:** Titles and priorities are preserved from `parabank_manual_testing.xlsx`. Scenario order is independent of TestRail numbering.
- **Overlapping checks:** TS-008 overlaps with TS-042 and TS-043; all existing cases are retained.
- **Password changes:** TS-039 and TS-040 depend on password-change functionality being available in the tested build. Record a scope limitation if it is unavailable.
- **Business rules:** Confirm rules for zero amounts, same-account transfers, and overdrafts before reporting a defect.
- **Session checks:** Distinguish a cached page from restored authenticated access by attempting to use protected functionality.
