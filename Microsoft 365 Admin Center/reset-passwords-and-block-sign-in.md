


# ☁️ Microsoft 365 - Reset Password and Block Sign-In

[ Back to Overview] → [README.md](./README.md)

---

## 📋 Summary

Reset a user's password and block a user from signing in, using the Microsoft 365 Admin Center. A password reset is one of the most common help desk tickets, and blocking sign-in is the quick, reversible way to stop access, for example when an account may be compromised or an employee leaves.

---

## 💡 Reset Password and Block Sign-In

| | Reset password | Block sign-in |
|---|----------------|---------------|
| **Purpose** | Give a user who forgot the password a new temporary one | Stop the user from signing in, without deleting the account |
| **Account data** | Unchanged | Unchanged. The mailbox, files and licence stay in place |
| **Reversible** | Not applicable | Yes, untick the option to unblock |
| **Typical ticket** | "I forgot my password" | "Block this account now" |

| Setting | Value |
|---------|-------|
| **Tool** | Microsoft 365 Admin Center (`admin.microsoft.com`) |
| **User** | Asha Mallik |
| **Location** | Users → Active users → the user |

### Prerequisites

- An account with permission to reset passwords and manage users, such as **Helpdesk Administrator**, **User Administrator** or **Global Administrator**
- The correct user account, identified and verified

> **Verify the caller first.** Before you reset a password or block an account, confirm the requester's identity using your company's process, for example a callback to a registered number or an approval from the user's manager. An attacker who asks for a password reset is a common attack.

---

## 🔧 Part 1 - Reset a Password

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Go to **Users → Active users**.
3. Select the user account.
4. Click **Reset password** in the top menu.
5. Choose **Automatically create a password**, or **Let me create the password** and enter a temporary one.
6. Tick **Require this user to change their password when they first sign in**.
7. Click **Reset**.
8. Copy the temporary password from the confirmation page, and give it to the user through a secure channel, such as a verified phone call.

> Never show the temporary password in a screenshot or in the repository.

**Screenshots: resetting the password:**

<img width="1920" height="1080" alt="Active users list with the user selected and the Reset password button" src="https://github.com/user-attachments/assets/b4ca2f4b-2400-4fd9-9b53-7235a3782d9e" />

<img width="1920" height="1080" alt="Reset password pane with the password options" src="https://github.com/user-attachments/assets/a9dc60ff-e859-48e6-8b51-428d87d236dc" />

<img width="1920" height="1080" alt="Require this user to change their password when they first sign in ticked" src="https://github.com/user-attachments/assets/a5bfe48a-2552-4e85-b5b3-0d4456074d96" />

<img width="1920" height="1080" alt="Confirmation that the password was reset" src="https://github.com/user-attachments/assets/e02dd61b-b445-4386-a237-2562e63d55ea" />

**Expected result:** The password is reset. The user signs in with the temporary password and is asked to choose a new one.

---

## 🔧 Part 2 - Block Sign-In

1. Go to **Users → Active users**.
2. Select the user account.
3. Choose **Block sign-in**.
4. Tick **Block this user from signing in**.
5. Click **Save changes**.

**Screenshots: blocking sign-in:**

<img width="1920" height="1080" alt="The user's panel with the Block sign-in option" src="https://github.com/user-attachments/assets/0c6b7ecc-6526-4041-af85-31548fcd4ad1" />

<img width="1920" height="1080" alt="Block this user from signing in ticked" src="https://github.com/user-attachments/assets/bf16a2d7-5b58-4a13-92dd-8430a0e87056" />

<img width="1920" height="1080" alt="The user shown as blocked from signing in" src="https://github.com/user-attachments/assets/57f862bd-0ceb-4e23-bbf5-9c531a3e951e" />

<img width="1920" height="1080" alt="Sign-in status showing the user is blocked" src="https://github.com/user-attachments/assets/d7814b2f-23e9-4a9e-a83b-bbaceb5802ac" />


<img width="1920" height="1080" alt="Sign-in with the temporary password and the request to change it" src="https://github.com/user-attachments/assets/da515add-b3ce-491a-a166-a542d886ea22" />
**Expected result:** The account cannot start new sign-ins after the change takes effect. The account, the mailbox and the licence stay in place.

> **Existing sessions:** A user who is already signed in may stay signed in for a while. If access must end at once, also sign the user out of all sessions. The option is in the user's panel (for example on the **Account** tab). Where you must act immediately, also reset the password.
>
> **To unblock:** Open the same option, untick **Block this user from signing in** and click **Save changes**.


**Screenshots: results:**

 <img width="1920" height="1080" alt="Sign-in refused for the blocked account" src="https://github.com/user-attachments/assets/90fda808-58d1-480f-9162-2205878653a5" />


---





---
## ✅ Verification

| Check | Where | Expected Result |
|-------|-------|-----------------|
| Password reset | Admin Center | The confirmation page shows the reset ✅ |
| Sign-in with the new password | Sign in at `office.com` as the user (use a private browser window) | The temporary password is accepted, and Microsoft asks for a new password ✅ |
| Sign-in blocked | The user's panel | The sign-in status shows **Blocked** ✅ |
| Sign-in refused | Sign in at `office.com` as the blocked user | Sign-in fails with a message that the account is disabled or locked ✅ |

---

## 🛠️ Common Problems

| Problem | Likely cause | What to check |
|---------|--------------|---------------|
| **Reset password is greyed out** | You lack permission, or the account is synced from on-premises Active Directory | Check your admin role. For synced accounts, reset the password in Active Directory |
| **The user cannot sign in with the new password** | The password was typed wrongly, or the user is blocked | Reset it again, and check the sign-in status |
| **The user says they never got the password** | The temporary password was not delivered | Reset it again, and deliver it through a secure channel |
| **The blocked user is still using the account** | The existing session is still active | Sign the user out of all sessions, and reset the password |
| **The user cannot sign in after unblocking** | The block was not saved, or the password also needs a reset | Check the sign-in status and reset the password |
| **Password reset asks for extra verification** | A policy requires multi-factor authentication for admins | Complete the verification with your admin account |

---

## 💡 Next Step

→ [Delete and Restore a User Account](./delete-restore-user-m365.md)



