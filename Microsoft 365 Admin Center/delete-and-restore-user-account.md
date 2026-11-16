# ☁️ Microsoft 365 - Delete and Restore a User Account

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Delete a user account in the Microsoft 365 Admin Center, then restore it from **Deleted users**. Deleting and restoring accounts is a regular task for an IT Help Desk Tier 1 and Tier 2 technician, for example when an employee leaves, or when an account was deleted by mistake.

---

## 💡 What Happens When You Delete a User?

A deleted user is not removed straight away. The account moves to **Deleted users** and is kept for **30 days**, so it can be restored. After 30 days it is deleted permanently and cannot be restored.

| | While in Deleted users (up to 30 days) | After 30 days |
|---|----------------------------------------|---------------|
| **Sign-in** | Blocked | Not possible |
| **Licence** | Released, so it is free for another user | Not applicable |
| **Mailbox and OneDrive** | Kept for a limited time | Permanently removed |
| **Restore** | Possible | Not possible |

| Setting | Value |
|---------|-------|
| **Tool** | Microsoft 365 Admin Center (`admin.microsoft.com`) |
| **User** | Asha Mallik |
| **Location** | Users → Active users, and Users → Deleted users |

### Prerequisites

- An account with permission to manage users, such as **User Administrator** or **Global Administrator**
- The user account to delete or restore
- An available licence, if the restored user needs licensed services

> Accounts that are **synced from an on-premises Active Directory** cannot be deleted in the Admin Center. They are deleted in on-premises Active Directory and then removed from Microsoft 365 by the sync.

---

## 🔧 Part 1 - Delete a User

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Go to **Users → Active users**.
3. Tick the box next to the user account.
4. Click **Delete user**.
5. Read the confirmation message and confirm the deletion.

**Screenshots: deleting the user:**

<img width="1920" height="1080" alt="Active users list with the user selected" src="https://github.com/user-attachments/assets/377edc83-5a48-4354-aad4-e875690515f4" />

<img width="1920" height="1080" alt="Delete user confirmation window" src="https://github.com/user-attachments/assets/bc2d4b9a-833d-41de-a6f1-95c1868139b2" />

<img width="1920" height="1080" alt="The user shown in the Deleted users list" src="https://github.com/user-attachments/assets/db0e7c6b-7826-40bb-a72c-82f19b7aa9ba" />

**Expected result:** The user is no longer in **Active users**. The account is listed under **Deleted users**, and it can be restored within 30 days.

> **Before you delete a user:** Check whether the mailbox, OneDrive files or other data are needed. Follow your company's offboarding process first, for example giving the manager access to the files, or converting the mailbox.

---

## 🔧 Part 2 - Restore a User

1. Go to **Users → Deleted users**.
2. Select the user to restore.
3. Click **Restore user**.
4. Set a password for the restored account: choose **Auto-generate password** or enter a temporary one, and click **Restore**.
5. Copy the temporary password if it was auto-generated.
6. Assign a Microsoft 365 licence, if the user needs one: open **Users → Active users**, select the user, then **Licenses and apps**, tick the licence and click **Save changes**.

> The temporary password must never be shown in a screenshot or in the repository.

**Screenshots: restoring the user:**

<img width="1920" height="1080" alt="Deleted users list with the user selected and the Restore user button" src="https://github.com/user-attachments/assets/ae42c590-6391-4531-81a1-cda629846a9d" />

<img width="1920" height="1080" alt="Restore user window with the password options" src="https://github.com/user-attachments/assets/1dd81ee5-6829-4ff4-8d70-f4852847c9f7" />

<img width="1920" height="1080" alt="Confirmation that the user was restored" src="https://github.com/user-attachments/assets/0d0b2e66-8303-4c98-8ac9-04c3da185961" />



<img width="1920" height="1080" alt="Active users list showing the restored user" src="https://github.com/user-attachments/assets/33f8ce14-68db-4fb5-b122-d1d3cacd1395" />


**Expected result:** The account returns to **Active users**. The restored user has **no licence** until you assign one, so the services, such as the mailbox, come back after the licence is assigned.

---



**Screenshots: restored account:**



<img width="1920" height="1080" alt="The restored user's Licenses and apps tab" src="https://github.com/user-attachments/assets/9aaca07c-8010-45a1-876b-b14d7cc8192c" />

---


## ✅ Verification

| Check | Where | Expected Result |
|-------|-------|-----------------|
| User deleted | Users → Deleted users | The user is listed ✅ |
| User restored | Users → Active users | The user is listed again, with the same username ✅ |
| Licence assigned | User → **Licenses and apps** | The licence is ticked ✅ |
| Access restored | Sign in at `office.com` as the user (use a private browser window) | The password is accepted and the apps and the mailbox are available ✅ |

---

## 🛠️ Common Problems

| Problem | Likely cause | What to check |
|---------|--------------|---------------|
| **The user is not in Deleted users** | The account was deleted more than 30 days ago, or it is a synced account | If it was more than 30 days ago, the account must be created again. For synced accounts, check on-premises Active Directory |
| **The Delete user button is greyed out** | The account is synced from on-premises Active Directory, or you lack permission | Delete it in Active Directory, and check your admin role |
| **The restored user cannot use the mailbox or apps** | The licence was released when the user was deleted | Assign a licence in **Licenses and apps**, and wait a few minutes |
| **The user cannot sign in after the restore** | The temporary password was not given to the user | Reset the password, and have the user change it at the first sign-in |
| **Restore shows an error** | A conflict, for example another account now uses the same username | Read the message, and change the username of the other account or the restored one |

---

## 💡 Next Step

→ [Reset a User Password in Microsoft 365](./reset-password-m365.md)





































