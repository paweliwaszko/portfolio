[Test_Plan_PKO_Internet_Banking.md](https://github.com/user-attachments/files/31916863/Test_Plan_PKO_Internet_Banking.md)
# Test Plan – PKO Bank Polski Internet Banking (Portfolio Project)

| | |
|---|---|
| **Document Version** | 1.0 |
| **Author** | Paweł |
| **Date** | 07 September 2026 |
| **Project Type** | Manual Testing Portfolio Project |

> **Disclaimer:** This is an independent portfolio project created for educational purposes. It is not affiliated with, endorsed by, or conducted on behalf of PKO Bank Polski.

---

## 1. Objective

The objective of this testing activity is to verify that the core user-facing functionalities of an online banking application work correctly, provide appropriate validation, and deliver a reliable user experience.

The focus is on **functional testing** of essential banking operations from a customer's perspective.

---

## 2. Scope

### 2.1 In Scope
- Login page and authentication validation
- Dashboard overview
- Account balance display
- Transaction history
- Money transfer form and validation
- Logout functionality
- Basic responsive behavior

### 2.2 Out of Scope
- Internal banking systems
- Payment processing infrastructure
- Security / penetration testing
- Performance testing
- Mobile application (native app)
- Administrative features

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

---

## 6. Test Data

| Data | Purpose |
|---|---|
| Valid test credentials | Login |
| Invalid password | Negative login |
| Invalid account number | Transfer validation |
| Empty required fields | Validation testing |
| Various transfer amounts | Boundary testing |

---

## 7. Features to Be Tested

### 7.1 Authentication
- Successful login
- Invalid password
- Empty username
- Empty password
- Error message verification

### 7.2 Dashboard
- Account balance visibility
- Navigation availability
- Basic page loading

### 7.3 Transaction History
- Transaction list display
- Transaction details
- Date consistency

### 7.4 Money Transfer
- Valid transfer data
- Invalid account number
- Empty mandatory fields
- Zero amount
- Maximum allowed values (validation)

### 7.5 Logout
- Manual logout
- Session termination
- Back button behavior after logout

---

## 8. Entry Criteria

Testing begins when:
- The application is accessible.
- The test environment is available.
- Test credentials are prepared.
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
| UI changes during testing | Medium |
| Temporary service unavailability | High |
| Browser compatibility issues | Medium |
| Session expiration | Low |

---

## 11. Test Priorities

| Priority | Area |
|---|---|
| Critical | Login |
| Critical | Money Transfer |
| High | Dashboard |
| High | Transaction History |
| Medium | Logout |
| Medium | Responsive Layout |

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

- Testing is performed from the perspective of an end user.
- No real financial transactions are intentionally executed.
- The project focuses on demonstrating manual testing methodology rather than auditing the banking system itself.

Add Test Plan for banking application
