# BUG-005 — Bill Payment Can Be Completed With a Negative Amount

## Bug Details

| Field | Value |
|---|---|
| **Bug ID** | BUG-005 |
| **Module** | Bill Pay |
| **Type** | Validation / Functional |
| **Priority** | High |
| **Status** | Open |
| **Related Test Case** | T138 — Bill payment with negative amount |

## Description

The Bill Pay functionality accepts a negative payment amount.

A user can submit a payment with a value such as **-$100.00**, and the application processes it successfully instead of rejecting the invalid value.

## Preconditions

- The user is logged in to ParaBank.
- The Bill Pay page is accessible.
- A valid source account is available.

## Steps to Reproduce

1. Log in to ParaBank.
2. Navigate to **Bill Pay**.
3. Enter valid payee information.
4. Enter matching account numbers.
5. Enter `-100` in the **Amount** field.
6. Select an account to pay from.
7. Click **Send Payment**.

## Expected Result

The payment should be rejected.

Negative values should not be accepted as valid payment amounts and no payment should be processed.

## Actual Result

The application accepts the negative amount and completes the bill payment successfully.

## Environment

- **Application:** ParaBank Demo
- **Platform:** Web
- **Operating System:** Windows 11
- **Browser:** Google Chrome

## Evidence

Screenshot showing the successful bill payment with a negative amount.

![BUG-005 Evidence](../screenshots/BUG-005.png)
