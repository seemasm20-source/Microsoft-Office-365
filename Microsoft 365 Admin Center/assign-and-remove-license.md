# ☁️ Microsoft 365 - Assign and Remove Licences

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Assign a Microsoft 365 licence to a user, and remove a licence from a user, in the Microsoft 365 Admin Center. Licence changes are a daily task for an IT Help Desk Tier 1 and Tier 2 technician, for example when a new employee needs email and Office apps, or when someone leaves the company.

---

## 💡 What is a Licence?

A licence gives a user access to Microsoft 365 services, such as an Exchange mailbox, Teams, OneDrive and the Office apps. A user without a licence can sign in, but cannot use the licensed services. Each licence is paid for, so a company has a limited number of them.

| Setting | Value |
|---------|-------|
| **Tool** | Microsoft 365 Admin Center (`admin.microsoft.com`) |
| **User** | Asha Mallik |
| **Licence assigned** | Office 365 E5 |
| **Location** | Users → Active users → the user → **Licenses and apps** |

### Prerequisites

- An account with permission to manage licences, such as **License Administrator**, **User Administrator** or **Global Administrator**
- An available licence for the assignment
- A **usage location** set on the user. Microsoft needs it before it assigns a licence

> The wording on screen is **Licenses and apps**.

---

## 🔧 Part 1 - Assign a Licence

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Go to **Users → Active users**.
3. Select the user.
4. Open the **Licenses and apps** tab.
5. Select the **Location** if it is empty.
6. Tick the licence, here **Office 365 E5**.
7. Click **Save changes**.

**Screenshots: assigning the licence:**

<img width="1920" height="1080" alt="Active users list with the user selected" src="https://github.com/user-attachments/assets/dbf1052e-9b42-445d-a0c0-d4f91d8b7f3d" />

<img width="1920" height="1080" alt="The Licenses and apps tab of the user" src="https://github.com/user-attachments/assets/508ec073-158c-44cf-b74e-1577b6f6bb9c" />

<img width="1920" height="1080" alt="Office 365 E5 ticked and Save changes selected" src="https://github.com/user-attachments/assets/6e8eaef5-9f6d-4365-a6e8-264854ebbe2a" />

**Expected result:** The licence is assigned to the user, and the number of **available** licences goes down by one.

> A licence can take a few minutes, and sometimes longer, before the services such as the mailbox are ready for the user.

---

## 🔧 Part 2 - Remove a Licence

1. Go to **Users → Active users**.
2. Select the user.
3. Open the **Licenses and apps** tab.
4. **Untick** the licence you want to remove.
5. Click **Save changes**.

**Screenshots: removing the licence:**

<img width="1920" height="1080" alt="The Licenses and apps tab with the licence ticked" src="https://github.com/user-attachments/assets/aac3a206-4c0e-40fd-bee0-ce2aef3a3870" />

<img width="1920" height="1080" alt="The licence unticked and Save changes selected" src="https://github.com/user-attachments/assets/198ff480-f948-4ea8-92b8-93e29bb697b7" />


<img width="1920" height="1080" alt="The Licenses and apps tab showing the final licence status" src="https://github.com/user-attachments/assets/5df8efab-32b8-4e48-93ba-af4b48419999" />

**Expected result:** The licence is removed from the user, and the number of **available** licences goes up by one.

> **Before you remove a licence:** The user loses access to the services in it, such as the mailbox and Office apps. Some data, such as the mailbox, is kept for a limited time and can be lost if the licence stays removed. If the user is leaving, follow your company's offboarding process first, for example converting the mailbox or keeping the data, before you remove the licence.

---



**Screenshot: licence status after the change:**






<img width="1920" height="1080" alt="The licence list showing the number of available licences" src="https://github.com/user-attachments/assets/c01b360c-37ba-4192-8dc5-311ec013b745" />

---

## ✅ Verification

| Check | Where | Expected Result |
|-------|-------|-----------------|
| Licence assigned | User → **Licenses and apps** | Office 365 E5 is ticked ✅ |
| Licence count | Admin Center → **Billing → Licenses** | **Available** licences went down by one ✅ |
| Services available | Sign in as the user at `office.com` (use a private browser window) | The apps and the mailbox are available ✅ |
| Licence removed | User → **Licenses and apps** | Office 365 E5 is no longer ticked ✅ |

---

## 🛠️ Common Licence Problems

| Problem | Likely cause | What to check |
|---------|--------------|---------------|
| **The licence is greyed out or shows 0 available** | All licences are in use | Billing → Licenses. Free one by removing it from another user, or buy more |
| **Cannot assign a licence: location is missing** | The user has no usage location | Set the **Location** on the **Licenses and apps** tab, then save |
| **Cannot untick a licence** | The licence comes from a **group** (group-based licensing) | Remove the user from the licensing group, or change the group's licences |
| **User has the licence but no mailbox or apps yet** | The services are still being set up | Wait a few minutes, and check again |
| **Save changes shows an error** | A conflict or missing requirement | Read the message, and check the location and the licence count |

---

## 💡 Next Step

→ [Reset Passwords and Block Sign-In](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Microsoft%20365%20Admin%20Center/reset-passwords-and-block-sign-in.md)







































































































