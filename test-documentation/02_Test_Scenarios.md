# 🧪 ParaBank — Test Scenarios

## 📌 Project Overview

This document presents the manual test scenarios prepared for the ParaBank demo application.

The scenarios are organized according to the same functional sections used in TestRail.

| Project Information | Details |
|---|---|
| **Project** | ParaBank Manual Testing |
| **Application** | ParaBank Demo |
| **Testing Type** | Manual Functional Testing |
| **Test Management Tool** | TestRail |
| **Total Test Cases** | 45 |
| **Functional Sections** | 7 |

---

# 01 — 🔐 Login

## TS-001 — Verify Login Functionality

### 🎯 Objective

Verify that the application correctly handles user authentication using valid, invalid, incomplete, and potentially malicious login data.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C46** | Login with valid credentials |
| **C47** | Login with invalid password |
| **C48** | Login with invalid username |
| **C49** | Login with empty username |
| **C50** | Login with empty password |
| **C51** | Login with SQL injection attempt |
| **C52** | Verify successful logout after login |
| **C90** | Login with empty username and password |

### ✅ Expected Behavior

- Valid credentials allow the user to log in.
- Invalid credentials do not provide access to the application.
- Required login fields are properly validated.
- SQL injection attempts do not bypass authentication.
- A logged-in user can successfully log out.

---

# 02 — 👤 Registration

## TS-002 — Verify User Registration

### 🎯 Objective

Verify that new users can register successfully and that the registration form correctly handles invalid or incomplete data.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C53** | Register a new user with valid data |
| **C54** | Registration with all required fields empty |
| **C55** | Registration with mismatched passwords |
| **C56** | Registration with an existing username |
| **C57** | Registration with empty username |
| **C58** | Registration with empty password |

### ✅ Expected Behavior

- A new user can register with valid and unique data.
- Required fields cannot be left empty.
- Password and password confirmation must match.
- Existing usernames cannot be reused.
- Registration is blocked when mandatory credentials are missing.

---

# 03 — 💳 Accounts

## TS-003 — Verify Account Information and Transaction History

### 🎯 Objective

Verify that authenticated users can access their accounts, view account details, review transaction history, and use transaction filters.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C59** | View Accounts Overview after successful login |
| **C60** | View account details |
| **C61** | View transaction history for an account |
| **C62** | View transaction details |
| **C63** | Filter transactions by activity period |
| **C64** | Filter transactions by transaction type |

### ✅ Expected Behavior

- The Accounts Overview page displays available user accounts.
- Account details can be opened successfully.
- Transaction history is displayed for the selected account.
- Individual transaction details are accessible.
- Activity period filtering displays only matching transactions.
- Transaction type filtering displays only matching transaction types.

---

# 04 — 💸 Fund Transfer

## TS-004 — Verify Fund Transfer Functionality

### 🎯 Objective

Verify that transfers between accounts work correctly and that the application properly handles valid and invalid transfer amounts.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C65** | Transfer funds between accounts with valid data |
| **C66** | Transfer funds with empty amount |
| **C67** | Transfer funds with zero amount |
| **C68** | Transfer funds with negative amount |
| **C69** | Transfer funds with invalid amount format |
| **C70** | Transfer funds with valid decimal amount |
| **C71** | Transfer funds using the same source and destination account |
| **C72** | Transfer amount greater than available balance |
| **C73** | Verify account balances after successful fund transfer |
| **C74** | Verify transaction history after successful fund transfer |

### ✅ Expected Behavior

- Valid transfers are completed successfully.
- Decimal amounts are processed correctly.
- Empty, zero, negative, and invalid amounts are rejected.
- The application prevents invalid transfers between the same account.
- Transfers exceeding the available balance are rejected.
- Account balances are updated correctly after successful transfers.
- Completed transfers appear in transaction history.

---

# 05 — 🧾 Bill Payment

## TS-005 — Verify Bill Payment Functionality

### 🎯 Objective

Verify that users can complete valid bill payments and that invalid payment information is properly validated.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C75** | Pay a bill with valid data |
| **C76** | Bill payment with all required fields empty |
| **C77** | Bill payment with mismatched account numbers |
| **C78** | Bill payment with zero amount |
| **C79** | Bill payment with negative amount |
| **C80** | Bill payment with invalid amount format |

### ✅ Expected Behavior

- A bill payment with valid data is completed successfully.
- Required fields cannot be empty.
- Account number and confirmation account number must match.
- Zero and negative payment amounts are rejected.
- Invalid amount formats are rejected.
- Appropriate validation messages are displayed for invalid input.

---

# 06 — 👤 Profile & Password

## TS-006 — Verify Profile Information Functionality

### 🎯 Objective

Verify that profile information is displayed correctly, can be updated using valid data, and that invalid profile data is handled appropriately.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C81** | Update profile information with valid data |
| **C82** | Update profile with required fields empty |
| **C83** | Verify current profile information is displayed correctly |
| **C84** | Update profile with invalid ZIP code |
| **C85** | Verify updated profile data persists after re-login |

### ✅ Expected Behavior

- Current profile information is displayed correctly.
- Valid profile changes can be saved.
- Required fields are properly validated.
- Invalid ZIP Code values are rejected with an appropriate message.
- Updated profile information persists after logout and re-login.
- Invalid input should not cause an internal application error.

> **Note:** The TestRail section retains the name **Profile & Password**, although the current ParaBank version used during testing does not provide password-change functionality.

---

# 07 — 🚪 Logout & Session

## TS-007 — Verify Logout and Session Management

### 🎯 Objective

Verify that users can log out successfully, protected pages remain inaccessible after logout, and authenticated sessions behave correctly during navigation.

### 🧾 Covered Test Cases

| Case ID | Test Case |
|---|---|
| **C86** | Successful logout |
| **C87** | Access protected page after logout |
| **C88** | Access protected page using direct URL after logout |
| **C89** | Verify session remains active during authenticated navigation |

### ✅ Expected Behavior

- The user can log out successfully.
- The authenticated session is terminated after logout.
- Protected functionality cannot be accessed after logout.
- Direct access to protected URLs does not restore access.
- Unauthorized access attempts are handled with an appropriate authentication message or redirect.
- The authenticated session remains active during normal navigation.

---

# 📊 Test Scenario Summary

| Scenario ID | TestRail Section | Test Cases |
|---|---|---:|
| **TS-001** | Login | 8 |
| **TS-002** | Registration | 6 |
| **TS-003** | Accounts | 6 |
| **TS-004** | Fund Transfer | 10 |
| **TS-005** | Bill Payment | 6 |
| **TS-006** | Profile & Password | 5 |
| **TS-007** | Logout & Session | 4 |
|  | **TOTAL** | **45** |

---

## 📝 Notes

- Test cases are maintained in **TestRail**.
- Scenario categories correspond directly to the TestRail sections.
- Failed test cases are documented in the `bug-reports/` directory.
- Evidence is stored in the `screenshots/` directory.
- Test execution results will be summarized in the Test Summary Report.
