# 🧪 ParaBank — Test Scenarios

## 📌 Project Overview

This document contains the manual test scenarios prepared for the ParaBank demo application.

The scenarios cover the main business areas of the application, including authentication, registration, account management, fund transfers, bill payments, profile management, and session handling.

| Project Information | Details |
|---|---|
| **Project** | ParaBank Manual Testing |
| **Application** | ParaBank Demo |
| **Testing Type** | Manual Functional Testing |
| **Test Management Tool** | TestRail |
| **Total Test Scenarios** | 15 |
| **Total Test Cases** | 45 |

---

# 🔐 TS-001 — Login Functionality

### 🎯 Objective

Verify that users can log in with valid credentials and that the application correctly handles invalid, incomplete, and potentially malicious login attempts.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
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

- A registered user can log in using valid credentials.
- Invalid credentials do not allow access to the application.
- Empty fields are properly validated.
- SQL injection attempts do not bypass authentication.
- The user can successfully log out after login.

---

# 👤 TS-002 — User Registration

### 🎯 Objective

Verify that a new user can successfully create an account and that the registration form properly validates incorrect or incomplete data.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
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
- Password and confirmation password must match.
- An existing username cannot be reused.
- Registration is blocked when mandatory data is missing.

---

# 💳 TS-003 — Accounts Overview & Details

### 🎯 Objective

Verify that authenticated users can access their accounts and review account and transaction information.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C59** | View Accounts Overview after successful login |
| **C60** | View account details |
| **C61** | View transaction history for an account |
| **C62** | View transaction details |

### ✅ Expected Behavior

- The Accounts Overview page displays the user's accounts.
- Account details can be opened successfully.
- Transaction history is available for the selected account.
- Individual transaction details can be viewed.

---

# 🔎 TS-004 — Transaction History Filtering

### 🎯 Objective

Verify that users can correctly filter transaction history using the available filtering options.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C63** | Filter transactions by activity period |
| **C64** | Filter transactions by transaction type |

### ✅ Expected Behavior

- Only transactions matching the selected activity period are displayed.
- Only transactions matching the selected transaction type are displayed.
- Transactions outside the selected criteria are excluded.

---

# 💸 TS-005 — Successful Fund Transfer

### 🎯 Objective

Verify that funds can be transferred successfully between available accounts using valid data.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C65** | Transfer funds between accounts with valid data |
| **C70** | Transfer funds with valid decimal amount |
| **C73** | Verify account balances after successful fund transfer |
| **C74** | Verify transaction history after successful fund transfer |

### ✅ Expected Behavior

- A valid transfer is completed successfully.
- Decimal transfer amounts are processed correctly.
- Account balances are updated after the transfer.
- The transaction appears in transaction history.

---

# ⚠️ TS-006 — Fund Transfer Validation

### 🎯 Objective

Verify that invalid transfer amounts are properly rejected by the application.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C66** | Transfer funds with empty amount |
| **C67** | Transfer funds with zero amount |
| **C68** | Transfer funds with negative amount |
| **C69** | Transfer funds with invalid amount format |
| **C72** | Transfer amount greater than available balance |

### ✅ Expected Behavior

- Empty amounts are rejected.
- Zero-value transfers are rejected.
- Negative amounts are rejected.
- Invalid amount formats are rejected.
- Transfers exceeding the available balance are prevented.
- Appropriate validation messages are displayed.

---

# 🔄 TS-007 — Transfer Between the Same Account

### 🎯 Objective

Verify how the application handles a transfer when the same account is selected as both the source and destination.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C71** | Transfer funds using the same source and destination account |

### ✅ Expected Behavior

- The transfer should not be processed.
- The application should display an appropriate validation message.

---

# 🧾 TS-008 — Successful Bill Payment

### 🎯 Objective

Verify that a user can successfully make a bill payment using valid payee and payment information.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C75** | Pay a bill with valid data |

### ✅ Expected Behavior

- The payment is completed successfully.
- A payment confirmation is displayed.
- The correct account is used for the transaction.

---

# 🚫 TS-009 — Bill Payment Validation

### 🎯 Objective

Verify that the Bill Pay functionality correctly handles missing, inconsistent, and invalid payment data.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C76** | Bill payment with all required fields empty |
| **C77** | Bill payment with mismatched account numbers |
| **C78** | Bill payment with zero amount |
| **C79** | Bill payment with negative amount |
| **C80** | Bill payment with invalid amount format |

### ✅ Expected Behavior

- Required fields cannot be empty.
- Account number and confirmation account number must match.
- Zero payment amounts are rejected.
- Negative payment amounts are rejected.
- Invalid amount formats are rejected.
- Clear validation messages are displayed.

---

# 👤 TS-010 — Profile Information Display

### 🎯 Objective

Verify that the user's current profile information is displayed correctly.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C83** | Verify current profile information is displayed correctly |

### ✅ Expected Behavior

- The profile page displays the user's stored information.
- The displayed data matches the currently saved profile information.

---

# ✏️ TS-011 — Profile Information Update

### 🎯 Objective

Verify that users can update their profile information and that the changes remain saved after a new login session.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C81** | Update profile information with valid data |
| **C85** | Verify updated profile data persists after re-login |

### ✅ Expected Behavior

- Valid profile changes are saved successfully.
- Updated information is displayed after saving.
- Changes remain visible after logout and re-login.

---

# 🛑 TS-012 — Profile Form Validation

### 🎯 Objective

Verify that invalid or incomplete profile data is handled correctly.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C82** | Update profile with required fields empty |
| **C84** | Update profile with invalid ZIP code |

### ✅ Expected Behavior

- Required fields cannot be empty.
- Invalid ZIP Code values are rejected.
- Invalid data should not cause an internal application error.
- A clear validation message should be displayed.

---

# 🚪 TS-013 — Logout Functionality

### 🎯 Objective

Verify that an authenticated user can successfully log out of the application.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C86** | Successful logout |

### ✅ Expected Behavior

- The user is logged out successfully.
- The active authenticated session is terminated.
- The application returns the user to an unauthenticated state.

---

# 🔒 TS-014 — Protected Pages After Logout

### 🎯 Objective

Verify that protected functionality cannot be accessed after logout.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C87** | Access protected page after logout |
| **C88** | Access protected page using direct URL after logout |

### ✅ Expected Behavior

- Protected functionality is inaccessible after logout.
- Direct access using a protected URL does not restore access.
- The user is redirected to the login page or receives an authentication message.
- Unauthorized access should not cause an internal application error.

---

# 🌐 TS-015 — Authenticated Session Navigation

### 🎯 Objective

Verify that the authenticated session remains active while the user navigates between protected pages.

### 🧾 Covered Test Cases

| TestRail Case ID | Test Case |
|---|---|
| **C89** | Verify session remains active during authenticated navigation |

### ✅ Expected Behavior

- The user remains authenticated while navigating the application.
- The active session is not unexpectedly terminated.
- Protected pages remain accessible while the session is valid.

---

# 📊 Test Scenario Summary

| Scenario ID | Test Scenario | Test Cases |
|---|---|---:|
| **TS-001** | Login Functionality | 8 |
| **TS-002** | User Registration | 6 |
| **TS-003** | Accounts Overview & Details | 4 |
| **TS-004** | Transaction History Filtering | 2 |
| **TS-005** | Successful Fund Transfer | 4 |
| **TS-006** | Fund Transfer Validation | 5 |
| **TS-007** | Transfer Between the Same Account | 1 |
| **TS-008** | Successful Bill Payment | 1 |
| **TS-009** | Bill Payment Validation | 5 |
| **TS-010** | Profile Information Display | 1 |
| **TS-011** | Profile Information Update | 2 |
| **TS-012** | Profile Form Validation | 2 |
| **TS-013** | Logout Functionality | 1 |
| **TS-014** | Protected Pages After Logout | 2 |
| **TS-015** | Authenticated Session Navigation | 1 |
|  | **TOTAL** | **45** |

---

## 📝 Notes

- Test cases are managed in **TestRail**.
- Failed test cases are documented separately in the `bug-reports/` directory.
- Supporting screenshots are stored in the `screenshots/` directory.
- Test execution results are summarized in the final Test Summary Report.
