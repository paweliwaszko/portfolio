# ✅ ParaBank — Testing Checklist

## 📌 Overview

This checklist presents a high-level verification of the main functionalities of the **ParaBank Demo** application.

The checklist was executed during manual testing. Failed checks are linked directly to the corresponding bug reports.

### Status Legend

- ✅ **Passed** — functionality works as expected
- ❌ **Failed** — functionality does not work as expected
- ⛔ **Blocked** — test could not be completed due to another defect

---

## 🔐 01 — Login

| ID | Check | Status |
|---|---|---|
| C46 | Login with valid credentials | ✅ Passed |
| C47 | Login with invalid password | ✅ Passed |
| C48 | Login with invalid username | ✅ Passed |
| C49 | Login with empty username | ✅ Passed |
| C50 | Login with empty password | ✅ Passed |
| C51 | Login with SQL injection attempt | ✅ Passed |
| C52 | Verify successful logout after login | ✅ Passed |
| C90 | Login with empty username and password | ✅ Passed |

---

## 👤 02 — Registration

| ID | Check | Status |
|---|---|---|
| C53 | Register a new user with valid data | ✅ Passed |
| C54 | Registration with all required fields empty | ✅ Passed |
| C55 | Registration with mismatched passwords | ✅ Passed |
| C56 | Registration with an existing username | ✅ Passed |
| C57 | Registration with empty username | ✅ Passed |
| C58 | Registration with empty password | ✅ Passed |

---

## 💳 03 — Accounts

| ID | Check | Status |
|---|---|---|
| C59 | View Accounts Overview after successful login | ✅ Passed |
| C60 | View account details | ✅ Passed |
| C61 | View transaction history for an account | ✅ Passed |
| C62 | View transaction details | ✅ Passed |
| C63 | Filter transactions by activity period | ❌ Failed — [BUG-001](../bug-reports/BUG-001_Activity_Period_Filter.md) |
| C64 | Filter transactions by transaction type | ✅ Passed |

---

## 💸 04 — Fund Transfer

| ID | Check | Status |
|---|---|---|
| C65 | Transfer funds between accounts with valid data | ✅ Passed |
| C66 | Transfer funds with empty amount | ✅ Passed |
| C67 | Transfer funds with zero amount | ❌ Failed — [BUG-002](../bug-reports/BUG-002_Zero_Amount_Transfer.md) |
| C68 | Transfer funds with negative amount | ❌ Failed — [BUG-003](../bug-reports/BUG-003_Negative_Amount_Transfer.md) |
| C69 | Transfer funds with invalid amount format | ✅ Passed |
| C70 | Transfer funds with valid decimal amount | ✅ Passed |
| C71 | Transfer funds using the same source and destination account | ✅ Passed |
| C72 | Transfer amount greater than available balance | ✅ Passed |
| C73 | Verify account balances after successful fund transfer | ✅ Passed |
| C74 | Verify transaction history after successful fund transfer | ✅ Passed |

---

## 🧾 05 — Bill Payment

| ID | Check | Status |
|---|---|---|
| C75 | Pay a bill with valid data | ✅ Passed |
| C76 | Bill payment with all required fields empty | ✅ Passed |
| C77 | Bill payment with mismatched account numbers | ✅ Passed |
| C78 | Bill payment with zero amount | ❌ Failed — [BUG-004](../bug-reports/BUG-004_Zero_Amount_Bill_Payment.md) |
| C79 | Bill payment with negative amount | ❌ Failed — [BUG-005](../bug-reports/BUG-005_Negative_Amount_Bill_Payment.md) |
| C80 | Bill payment with invalid amount format | ✅ Passed |

---

## 👤 06 — Profile & Password

| ID | Check | Status |
|---|---|---|
| C81 | Update profile information with valid data | ❌ Failed — [BUG-006](../bug-reports/BUG-006_Profile_Update_Error.md) |
| C82 | Update profile with required fields empty | ✅ Passed |
| C83 | Verify current profile information is displayed correctly | ✅ Passed |
| C84 | Update profile with invalid ZIP code | ❌ Failed — [BUG-007](../bug-reports/BUG-007_Invalid_ZIP_Code_Error.md) |
| C85 | Verify updated profile data persists after re-login | ⛔ Blocked — [BUG-006](../bug-reports/BUG-006_Profile_Update_Error.md) |

> **Note:** The TestRail section retains the name **Profile & Password**, although the tested version of ParaBank does not provide password-change functionality.

---

## 🚪 07 — Logout & Session

| ID | Check | Status |
|---|---|---|
| C86 | Successful logout | ✅ Passed |
| C87 | Access protected page after logout | ✅ Passed |
| C88 | Access protected page using direct URL after logout | ❌ Failed — [BUG-008](../bug-reports/BUG-008_Direct_URL_After_Logout.md) |
| C89 | Verify session remains active during authenticated navigation | ✅ Passed |

---

# 📊 Checklist Summary

| Result | Number |
|---|---:|
| ✅ Passed | 36 |
| ❌ Failed | 8 |
| ⛔ Blocked | 1 |
| **Total** | **45** |

---

## 🐞 Defects

A total of **8 defects** were documented during test execution.

Detailed defect reports are available in the [`bug-reports`](../bug-reports/) directory.

Screenshot evidence for reported defects is available in the [`screenshots`](../screenshots/) directory.

---

## 📝 Notes

This checklist provides a high-level overview of the executed manual tests.

The IDs used in this checklist correspond directly to the **TestRail Case IDs**, allowing each checklist item to be easily matched with its detailed test case in TestRail.

Detailed test cases include preconditions, test steps, expected results, and execution results.
