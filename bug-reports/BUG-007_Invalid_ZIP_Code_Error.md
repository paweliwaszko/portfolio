# BUG-007 — Invalid ZIP Code Causes an Internal Application Error

## Bug Details

| Field | Value |
|---|---|
| **Bug ID** | BUG-007 |
| **Module** | Update Contact Info |
| **Type** | Validation / Error Handling |
| **Priority** | Medium |
| **Status** | Open |
| **Related Test Case** | T143 — Update profile with invalid ZIP code |

## Description

The application does not handle an invalid ZIP Code correctly.

When an invalid value is submitted in the ZIP Code field, the application displays an internal error instead of providing an appropriate validation message.

## Preconditions

- The user is logged in to ParaBank.
- The **Update Contact Info** page is accessible.

## Steps to Reproduce

1. Log in to ParaBank.
2. Navigate to **Update Contact Info**.
3. Enter valid data in the required profile fields.
4. Enter `ABC` in the **ZIP Code** field.
5. Click **Update Profile**.
6. Observe the application response.

## Expected Result

The profile should not be updated.

An appropriate validation message should inform the user that the ZIP Code value is invalid.

## Actual Result

The application displays the following error:

> Error!  
> An internal error has occurred and has been logged.

No user-friendly validation message is displayed.

## Environment

- **Application:** ParaBank Demo
- **Platform:** Web
- **Operating System:** Windows 11
- **Browser:** Google Chrome

## Evidence

Screenshot showing the internal application error.

![BUG-007 Evidence](../screenshots/BUG-007.png)
