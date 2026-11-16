
# ☁️ Microsoft 365 Admin Center - Create a New User

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Create a new user in the Microsoft 365 Admin Center, assign a product licence and set the first sign-in options. Creating users is one of the most common tasks for an IT Help Desk Tier 1 and Tier 2 technician, for example when a new employee joins.

---

## 💡 What Happens When You Create a User?

The Admin Center creates the account in **Microsoft Entra ID**, the cloud directory behind Microsoft 365. The **licence** decides which services the user gets, such as Exchange mailbox, Teams and Office apps. A user without a licence can sign in, but has no licensed services.

| Setting | Value |
|---------|-------|
| **Tool** | Microsoft 365 Admin Center (`admin.microsoft.com`) |
| **Tenant domain** | `golden535.onmicrosoft.com` |
| **First name / Last name** | Asha / Mallik |
| **Display name** | Asha Mallik |
| **Username** | `ashamallik@golden535.onmicrosoft.com` |
| **Job title** | Help Desk Administrator |
| **Password option** | Temporary password, change at first sign-in |

### Prerequisites

- An account with permission to manage users, such as **User Administrator** or **Global Administrator**
- An available Microsoft 365 licence, if the user needs licensed services

> The options you see depend on the organisation's subscription and on your admin role.

---

## 🔧 Steps

### Step 1 - Sign In to the Admin Center

1. Open the [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Sign in with an administrator account.

### Step 2 - Open Active Users

1. Go to **Users → Active users**.
2. Click **Add a user**.

**Screenshot: Active users page:**

<img width="1920" height="1080" alt="Microsoft 365 Admin Center Active users page with the Add a user button" src="https://github.com/user-attachments/assets/33a3ba3d-834f-4efc-ab46-db13e077eebf" />

### Step 3 - Enter the User Details (Basics)

| Field | Value |
|-------|-------|
| **First name** | Asha |
| **Last name** | Mallik |
| **Display name** | Asha Mallik |
| **Username** | `ashamallik` |
| **Domain** | `golden535.onmicrosoft.com` |

The username and the domain together form the sign-in address.

### Step 4 - Set the Password

1. Choose **Auto-generate password**, or **Let me create the password** and enter a temporary one that meets the password rules.
2. Tick **Require this user to change their password when they first sign in**.
3. Click **Next**.

> Give the temporary password to the user through a secure channel, and never show it in screenshots or in the repository.

**Screenshot: Basics and password:**

<img width="1920" height="1080" alt="Add a user wizard Basics page with the user details and password options" src="https://github.com/user-attachments/assets/468f44b4-d49f-4d62-ab31-0cd4b3ff4a15" />

### Step 5 - Assign a Product Licence

1. Select the user's **Location**. The location is required before a licence can be assigned.
2. Select an available Microsoft 365 licence.
3. Click **Next**.

> If no licence is available, choose **Create user without product license**. You can assign one later in **Users → Active users → the user → Licenses and apps**.

**Screenshot: Product licences:**

<img width="1920" height="1080" alt="Add a user wizard Product licenses page with a licence selected" src="https://github.com/user-attachments/assets/6e5ec1da-f9ca-41e4-aac5-447b26bef387" />

### Step 6 - Optional Settings

Open **Profile info** and enter the optional details:

| Field | Value |
|-------|-------|
| **Job title** | Help Desk Administrator |
| **Department** | Optional |
| **Office** | Optional |
| **Manager** | Optional |

The **Roles** section stays on **User (no administration access)**, so the new user gets no admin rights.

**Screenshot: Optional settings:**

<img width="1920" height="1080" alt="Add a user wizard Optional settings with the job title entered" src="https://github.com/user-attachments/assets/2208cdf5-babe-4c20-86cb-410cc66892f6" />

### Step 7 - Review and Create

1. Check the username, the licence and the settings.
2. Click **Finish adding**.
3. The confirmation page shows the new user's details. Copy the temporary password if it was auto-generated, then click **Close**.

**Screenshot: user created:**

<img width="1920" height="1080" alt="Active users list showing the new user Asha Mallik" src="https://github.com/user-attachments/assets/ac454841-d48c-4c9e-a33c-82f0029826d7" />

---

## ✅ Verification

| Check | Where | Expected Result |
|-------|-------|-----------------|
| User listed | Admin Center → Users → Active users | `Asha Mallik` is listed ✅ |
| Licence assigned | Select the user → **Licenses and apps** | The Microsoft 365 licence is ticked ✅ |
| Sign-in works | Sign in at `office.com` as the new user (use a private browser window) | The password is accepted and Microsoft asks for a new password ✅ |

---

## 💡 Next Step

→ [Reset a User Password in Microsoft 365](./reset-password-m365.md)





















































































