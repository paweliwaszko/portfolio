# 📊 ParaBank — Test Summary Report

## 📌 Overview

This document summarizes the results of manual functional testing performed on the **ParaBank Demo** application.

A total of **45 test cases** were executed using **TestRail**. The testing covered the main functional areas of the application, including authentication, registration, account management, fund transfers, bill payments, profile management, and session handling.

---

## 📊 Test Execution Summary

| Status | Test Cases | Percentage |
|---|---:|---:|
| ✅ Passed | 36 | 80.0% |
| ❌ Failed | 8 | 17.8% |
| ⛔ Blocked | 1 | 2.2% |
| **Total** | **45** | **100%** |

---

## 🧪 Test Results

### 🔐 01 — Login

| Case ID | Test Case | Result |
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

### 👤 02 — Registration

| Case ID | Test Case | Result |
|---|---|---|
| C53 | Register a new user with valid data | ✅ Passed |
| C54 | Registration with all required fields empty | ✅ Passed |
| C55 | Registration with mismatched passwords | ✅ Passed |
| C56 | Registration with an existing username | ✅ Passed |
| C57 | Registration with empty username | ✅ Passed |
| C58 | Registration with empty password | ✅ Passed |

---

### 💳 03 — Accounts

| Case ID | Test Case | Result |
|---|---|---|
| C59 | View Accounts Overview after successful login | ✅ Passed |
| C60 | View account details | ✅ Passed |
| C61 | View transaction history for an account | ✅ Passed |
| C62 | View transaction details | ✅ Passed |
| C63 | Filter transactions by activity period | ❌ Failed — [BUG-001](../bug-reports/BUG-001_Activity_Period_Filter.md) |
| C64 | Filter transactions by transaction type | ✅ Passed |

---

### 💸 04 — Fund Transfer

| Case ID | Test Case | Result |
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

### 🧾 05 — Bill Payment

| Case ID | Test Case | Result |
|---|---|---|
| C75 | Pay a bill with valid data | ✅ Passed |
| C76 | Bill payment with all required fields empty | ✅ Passed |
| C77 | Bill payment with mismatched account numbers | ✅ Passed |
| C78 | Bill payment with zero amount | ❌ Failed — [BUG-004](../bug-reports/BUG-004_Zero_Amount_Bill_Payment.md) |
| C79 | Bill payment with negative amount | ❌ Failed — [BUG-005](../bug-reports/BUG-005_Negative_Amount_Bill_Payment.md) |
| C80 | Bill payment with invalid amount format | ✅ Passed |

---

### 👤 06 — Profile & Password

| Case ID | Test Case | Result |
|---|---|---|
| C81 | Update profile information with valid data | ❌ Failed — [BUG-006](../bug-reports/BUG-006_Profile_Update_Error.md) |
| C82 | Update profile with required fields empty | ✅ Passed |
| C83 | Verify current profile information is displayed correctly | ✅ Passed |
| C84 | Update profile with invalid ZIP code | ❌ Failed — [BUG-007](../bug-reports/BUG-007_Invalid_ZIP_Code_Error.md) |
| C85 | Verify updated profile data persists after re-login | ⛔ Blocked — [BUG-006](../bug-reports/BUG-006_Profile_Update_Error.md) |

---

### 🚪 07 — Logout & Session

| Case ID | Test Case | Result |
|---|---|---|
| C86 | Successful logout | ✅ Passed |
| C87 | Access protected page after logout | ✅ Passed |
| C88 | Access protected page using direct URL after logout | ❌ Failed — [BUG-008](../bug-reports/BUG-008_Direct_URL_After_Logout.md) |
| C89 | Verify session remains active during authenticated navigation | ✅ Passed |

---

## 🐞 Defect Summary

During test execution, **8 defects** were identified and documented.

| Priority | Defects |
|---|---:|
| 🔴 High | 3 |
| 🟡 Medium | 5 |
| **Total** | **8** |

Detailed reports are available in the [`bug-reports`](../bug-reports/) directory.

---

## 🎯 Conclusion

The majority of the tested ParaBank functionality worked as expected, with **36 of 45 test cases passing successfully**.

The most significant issues were identified in:

- Fund transfer amount validation
- Bill payment amount validation
- Profile information updates
- Transaction history filtering
- Error handling and session-related behavior

A total of **8 defects** were documented, including **3 High-priority** and **5 Medium-priority** issues.

One test case was blocked because successful profile updating was required before profile data persistence could be verified.

Based on the test results, the application requires fixes in the identified areas followed by **retesting and regression testing**.
