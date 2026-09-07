# Test Scenarios – ParaBank

| | |
|---|---|
| **Document Version** | 1.0 |
| **Author** | Paweł |
| **Project Type** | Manual Testing Portfolio Project |
| **Related Document** | Test Plan – ParaBank Demo Platform |

> **Disclaimer:** This is an independent portfolio project created for educational purposes using the ParaBank demo application.

---

## 1. Overview

This document lists the test scenarios derived from the Test Plan, grouped by application area. Each scenario will be broken down into detailed test cases in the accompanying Test Cases document.

**Total scenarios:** 22 | **Critical:** 6 | **High:** 12 | **Medium:** 4

---

## 2. Test Scenarios

### 2.1 Registration

| ID | Test Scenario | Priority |
|---|---|---|
| TS-001 | Verify that a new user can register successfully with valid data | High |
| TS-002 | Verify validation of required fields during registration | High |

### 2.2 Login

| ID | Test Scenario | Priority |
|---|---|---|
| TS-003 | Verify that a registered user can log in with valid credentials | Critical |
| TS-004 | Verify that login fails when an incorrect username or password is provided | Critical |
| TS-005 | Verify validation when required login fields are empty | High |

### 2.3 Accounts Overview

| ID | Test Scenario | Priority |
|---|---|---|
| TS-006 | Verify that the user can view the Accounts Overview page | High |
| TS-007 | Verify that the user can view the balance of an account | Critical |
| TS-008 | Verify that the user can view account transaction details | High |

### 2.4 Open New Account

| ID | Test Scenario | Priority |
|---|---|---|
| TS-009 | Verify that the user can open a new bank account | High |

### 2.5 Fund Transfer

| ID | Test Scenario | Priority |
|---|---|---|
| TS-010 | Verify that the user can transfer money between eligible accounts | Critical |
| TS-011 | Verify transfer validation when required fields are missing | High |
| TS-012 | Verify transfer validation when an invalid amount is entered | High |

### 2.6 Bill Payment

| ID | Test Scenario | Priority |
|---|---|---|
| TS-013 | Verify that the user can make a bill payment using valid data | Critical |
| TS-014 | Verify bill payment validation with invalid or incomplete data | High |

### 2.7 Transaction Search

| ID | Test Scenario | Priority |
|---|---|---|
| TS-015 | Verify that the user can search for transactions | Medium |
| TS-016 | Verify that the user can view transaction details | Medium |

### 2.8 Profile & Password Management

| ID | Test Scenario | Priority |
|---|---|---|
| TS-017 | Verify that the user can update their profile information | Medium |
| TS-018 | Verify that the user can change their password | High |

### 2.9 Request Loan

| ID | Test Scenario | Priority |
|---|---|---|
| TS-019 | Verify that the user can submit a loan request with valid data | Medium |
| TS-020 | Verify loan request validation when required fields are missing | Medium |

### 2.10 Logout & Session Control

| ID | Test Scenario | Priority |
|---|---|---|
| TS-021 | Verify that the user can successfully log out | High |
| TS-022 | Verify that protected pages cannot be accessed after logout | High |

---

## 3. Priority Definitions

| Priority | Description |
|---|---|
| Critical | Functionality directly related to authentication or financial operations. |
| High | Important functionality that significantly affects the user experience. |
| Medium | Supporting functionality that does not block the main banking flow. |

---

## 4. Application Areas Covered

- User Registration
- Login
- Accounts Overview
- Account Details
- Account Balance
- Opening a New Account
- Fund Transfer
- Bill Payment
- Transaction Search
- Profile Management
- Password Management
- Loan Request
- Logout
- Session and Access Control

---

## 5. Test Approach

Scenarios will be tested using a combination of:
- Positive Testing
- Negative Testing
- Functional Testing
- Exploratory Testing
- Boundary Value Analysis
- Equivalence Partitioning
- Error Guessing
