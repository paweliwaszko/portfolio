# Test Plan – ParaBank Demo Platform (Portfolio Project)

| | |
|---|---|
| **Document Version** | 1.0 |
| **Author** | Paweł |
| **Date** | 07 September 2026 |
| **Project Type** | Manual Testing Portfolio Project |
| **Application Under Test** | ParaBank Demo Site (parabank.parasoft.com) |

> **Disclaimer:** ParaBank is a publicly available demo banking application provided by Parasoft for testing practice. This test plan is an independent portfolio project created for educational purposes and is not affiliated with or conducted on behalf of Parasoft.

---

## 1. Objective

The objective of this testing activity is to verify that the core user-facing functionalities of the ParaBank demo banking application work correctly, provide appropriate validation, and deliver a reliable user experience.

The focus is on **functional testing** of essential banking operations from a customer's perspective.

---

## 2. Scope

### 2.1 In Scope
- Registration page
- Login page and authentication validation
- Accounts Overview page
- Open New Account
- Transfer Funds
- Bill Pay
- Find Transactions
- Update Contact Info
- Request Loan
- Logout functionality
- Basic responsive behavior

### 2.2 Out of Scope
- Backend/database validation beyond UI-visible results
- Payment processing infrastructure
- Security / penetration testing
- Performance / load testing
- Mobile application (native app)
- Third-party integrations (e.g., ParaBank's SOAP/REST web services)

---

## 3. Test Objectives

Testing aims to verify:
1. Correct functionality of critical user flows
2. Proper validation of mandatory fields
3. Error handling and user feedback
4. Navigation between core pages
5. Consistent behavior across supported browsers
6. Basic responsiveness

---

## 4. Test Strategy

### 4.1 Test Types
- Functional Testing (Positive / Negative)
- Regression Testing (selected features)
- UI Testing
- Exploratory Testing

### 4.2 Test Design Techniques
- Equivalence Partitioning
- Boundary Value Analysis
- Error Guessing
- Exploratory Testing

---

## 5. Test Environment

| Component | Version / Detail |
|---|---|
| Operating System | Windows 11 |
| Google Chrome | Latest |
| Microsoft Edge | Latest |
| Mozilla Firefox | Latest |
| Screen Resolution | 1920×1080 |
| Mobile Check | Android device – Chrome Mobile |
| Test URL | https://parabank.parasoft.com/parabank/index.htm |

---

## 6. Test Data

| Data | Purpose |
|---|---|
| Newly registered test account | Login / Accounts Overview |
| Invalid username / password | Negative login |
| Invalid account number | Transfer / Bill Pay validation |
| Empty required fields | Validation testing |
| Various transfer and payment amounts | Boundary testing |
| Sample payee details (Bill Pay) | Bill payment testing |

---

## 7. Features to Be Tested

### 7.1 Registration
- Successful registration with valid data
- Duplicate username
- Empty mandatory fields
- Password/confirm password mismatch
- Field-level validation messages

### 7.2 Authentication
- Successful login
- Invalid password
- Empty username
- Empty password
- Error message verification

### 7.3 Accounts Overview
- Account list display
- Account balance visibility
- Navigation to account details
- Basic page loading

### 7.4 Open New Account
- Successful account creation (Checking/Savings)
- Account creation with insufficient funding source
- Confirmation message and new account ID display

### 7.5 Transfer Funds
- Valid transfer between own accounts
- Transfer with insufficient balance
- Empty mandatory fields
- Zero or negative amount
- Confirmation message accuracy

### 7.6 Bill Pay
- Valid bill payment
- Empty mandatory fields
- Invalid payee account details
- Zero or negative amount
- Confirmation message accuracy

### 7.7 Find Transactions
- Search by date
- Search by date range
- Search by amount
- Search by transaction ID
- No results found handling

### 7.8 Update Contact Info
- Successful update of profile details
- Empty mandatory fields
- Invalid data formats (e.g., phone, zip code)

### 7.9 Request Loan
- Loan approval scenario
- Loan denial scenario
- Empty mandatory fields

### 7.10 Logout
- Manual logout
- Session termination
- Back button behavior after logout

---

## 8. Entry Criteria

Testing begins when:
- The ParaBank demo site is accessible.
- The test environment is available.
- Test account(s) are registered/prepared.
- Browsers are updated.

---

## 9. Exit Criteria

Testing is considered complete when:
- All planned test cases have been executed.
- Critical and High severity defects have been documented.
- Test execution results have been summarized.
- No blocking issues prevent completion of the main user journey.

---

## 10. Risk Assessment

| Risk | Impact |
|---|---|
| Shared public demo environment (data reset/shared by other users) | High |
| UI changes during testing | Medium |
| Temporary service unavailability | High |
| Browser compatibility issues | Medium |
| Session expiration | Low |

---

## 11. Test Priorities

| Priority | Area |
|---|---|
| Critical | Login |
| Critical | Transfer Funds |
| Critical | Bill Pay |
| High | Accounts Overview |
| High | Registration |
| Medium | Find Transactions |
| Medium | Open New Account |
| Medium | Update Contact Info |
| Low | Request Loan |
| Low | Logout / Responsive Layout |

---

## 12. Deliverables

This portfolio project will include the following documentation:
1. Test Plan
2. Test Scenarios
3. Test Cases
4. Bug Reports
5. Testing Checklist
6. Test Summary Report

---

## 13. Assumptions

- Testing is performed from the perspective of an end user, using a self-registered ParaBank test account.
- No real financial transactions are involved, as ParaBank is a demo application with simulated data.
- Because ParaBank is a shared public demo environment, some data (e.g., other users' transactions) may be visible or inconsistent, and this is expected rather than treated as a defect.
- The project focuses on demonstrating manual testing methodology rather than auditing the ParaBank application itself.
