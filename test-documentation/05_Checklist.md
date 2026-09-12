# ✅ ParaBank — Manual Testing Checklist

## 📌 Overview

This checklist provides a quick verification of the main functionalities of the **ParaBank Demo** application.

It complements the detailed test cases maintained in **TestRail** and can be used for smoke, regression, and exploratory testing.

| Project Information | Details |
|---|---|
| **Project** | ParaBank Manual Testing |
| **Application** | ParaBank Demo |
| **Testing Type** | Manual Functional Testing |
| **Platform** | Web |
| **Test Management Tool** | TestRail |

---

# 🔐 01 — Login

- [ ] Login is successful with valid credentials
- [ ] Invalid username is rejected
- [ ] Invalid password is rejected
- [ ] Empty username is properly validated
- [ ] Empty password is properly validated
- [ ] Empty username and password are properly validated
- [ ] SQL injection attempt does not bypass authentication
- [ ] Logged-in user can successfully log out

---

# 👤 02 — Registration

- [ ] New user can register with valid and unique data
- [ ] Required registration fields are validated
- [ ] Registration is rejected when all required fields are empty
- [ ] Mismatched passwords are rejected
- [ ] Existing username cannot be registered again
- [ ] Empty username is properly validated
- [ ] Empty password is properly validated

---

# 💳 03 — Accounts

- [ ] Accounts Overview is displayed after successful login
- [ ] User accounts are displayed correctly
- [ ] Account details can be opened
- [ ] Account information is displayed correctly
- [ ] Transaction history is available
- [ ] Individual transaction details can be viewed
- [ ] Transactions can be filtered by activity period
- [ ] Transactions can be filtered by transaction type
- [ ] Filtering displays only transactions matching selected criteria

---

# 💸 04 — Fund Transfer

- [ ] Funds can be transferred between different accounts
- [ ] Valid transfer amount is accepted
- [ ] Valid decimal amount is accepted
- [ ] Empty transfer amount is rejected
- [ ] Zero transfer amount is rejected
- [ ] Negative transfer amount is rejected
- [ ] Invalid amount format is rejected
- [ ] Transfer between the same source and destination account is prevented
- [ ] Transfer exceeding available balance is rejected
- [ ] Source account balance is updated after successful transfer
- [ ] Destination account balance is updated after successful transfer
- [ ] Successful transfer appears in transaction history
- [ ] Appropriate validation messages are displayed for invalid transfer data

---

# 🧾 05 — Bill Payment

- [ ] Bill payment can be completed with valid data
- [ ] Required payee fields are validated
- [ ] Payment cannot be submitted with all required fields empty
- [ ] Mismatched account numbers are rejected
- [ ] Zero payment amount is rejected
- [ ] Negative payment amount is rejected
- [ ] Invalid payment amount format is rejected
- [ ] Valid payment displays confirmation
- [ ] Appropriate validation messages are displayed for invalid payment data

---

# 👤 06 — Profile & Password

- [ ] Current profile information is displayed correctly
- [ ] Profile information can be updated with valid data
- [ ] Updated profile information is saved correctly
- [ ] Required profile fields are validated
- [ ] Invalid ZIP Code is rejected
- [ ] Invalid profile data displays a user-friendly validation message
- [ ] Invalid profile data does not cause an internal application error
- [ ] Updated profile information persists after logout and re-login

> **Note:** The TestRail section retains the name **Profile & Password**, although the tested version of ParaBank does not provide password-change functionality.

---

# 🚪 07 — Logout & Session

- [ ] User can log out successfully
- [ ] Authenticated session is terminated after logout
- [ ] Protected functionality cannot be accessed after logout
- [ ] Protected page cannot be accessed using a direct URL after logout
- [ ] Unauthorized access is handled with an appropriate authentication message or redirect
- [ ] Unauthorized access does not cause an internal application error
- [ ] Session remains active during normal authenticated navigation
- [ ] Protected pages remain accessible while the session is valid

---

# 🌐 General UI & Usability

- [ ] Main navigation links work correctly
- [ ] Pages load without unexpected errors
- [ ] Forms contain appropriate labels
- [ ] Buttons perform the expected actions
- [ ] Error messages are understandable
- [ ] Success messages are displayed when appropriate
- [ ] User-entered data is displayed correctly
- [ ] No unexpected internal application errors are displayed

---

# 📊 Checklist Summary

| Area | Status |
|---|---|
| 🔐 Login | ⬜ Not Executed |
| 👤 Registration | ⬜ Not Executed |
| 💳 Accounts | ⬜ Not Executed |
| 💸 Fund Transfer | ⬜ Not Executed |
| 🧾 Bill Payment | ⬜ Not Executed |
| 👤 Profile & Password | ⬜ Not Executed |
| 🚪 Logout & Session | ⬜ Not Executed |
| 🌐 General UI & Usability | ⬜ Not Executed |

---

## 📝 Notes

This checklist is intended as a lightweight verification tool and does not replace the detailed test cases maintained in **TestRail**.

Detailed defects discovered during test execution are documented in the [`bug-reports`](../bug-reports/) directory.
