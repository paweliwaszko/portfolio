# BUG-008 — Accessing a Protected Page via Direct URL After Logout Causes an Internal Error

## Bug Details

| Field | Value |
|---|---|
| **Bug ID** | BUG-008 |
| **Module** | Authentication / Session Management |
| **Type** | Error Handling |
| **Priority** | Medium |
| **Status** | Open |
| **TestRail Case ID** | C88 |
| **TestRail Test ID** | T147 |
| **Related Test Case** | Access protected page using direct URL after logout |
| **Test Result** | Failed |

## Description

After logging out, accessing a protected ParaBank page directly through its URL results in an internal application error.

The protected functionality is not accessible, but the unauthorized request is not handled correctly from the user's perspective.

## Preconditions

- The user is logged in to ParaBank.
- A protected ParaBank page is open.
- The URL of the protected page is known.

## Steps to Reproduce

1. Log in to ParaBank.
2. Navigate to a protected page.
3. Copy the URL of the protected page.
4. Log out of ParaBank.
5. Paste the copied URL into the browser address bar.
6. Press **Enter**.
7. Observe the application response.

## Expected Result

The protected page should not be accessible.

The user should be redirected to the login page or receive an appropriate message indicating that authentication is required.

## Actual Result

Access to the protected functionality is denied, but the application displays:

> Error!  
> An internal error has occurred and has been logged.

## Environment

- **Application:** ParaBank Demo
- **Platform:** Web
- **Operating System:** Windows 11
- **Browser:** Google Chrome

## Impact

The access restriction itself works, but unauthorized access attempts are handled incorrectly and result in a generic internal application error.

