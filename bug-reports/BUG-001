# 🐞 BUG-001 — Transaction History Ignores Selected Activity Period

## Summary

The transaction history displays transactions outside the activity period selected by the user.

When **January** is selected from the **Activity Period** filter, a transaction from **September** is still displayed in the transaction list.

---

## Bug Details

| Field | Value |
|---|---|
| **Bug ID** | BUG-001 |
| **Module** | Accounts / Transaction History |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Type** | Functional |
| **Reproducibility** | 100% (3/3 attempts) |

---

## Environment

| Field | Value |
|---|---|
| **Application** | ParaBank Demo |
| **Platform** | Web |
| **Operating System** | Windows 11 |
| **Browser** | Google Chrome |

---

## Preconditions

- The user is logged in to ParaBank.
- The user has at least one bank account.
- The selected account contains a transaction from September.

---

## Steps to Reproduce

1. Log in to ParaBank.
2. Navigate to **Accounts Overview**.
3. Select an account containing transaction history.
4. Select **January** from the **Activity Period** dropdown.
5. Click the **Go** button.
6. Review the displayed transaction list.

---

## Expected Result

Only transactions matching the selected activity period (**January**) should be displayed.

---

## Actual Result

A transaction from **September** is displayed even though **January** is selected as the activity period.

---

## Evidence

Screenshot showing the selected **January** activity period and the transaction from **September**:

![BUG-001 - Incorrect activity period filtering](../../screenshots/BUG-001.png)

---

## Related Test Case

**Test Case:** Filter transactions by activity period  
**Test Result:** ❌ Failed

---

## Notes

The issue affects transaction history filtering and may cause users to receive incorrect results when reviewing transactions for a specific period.
