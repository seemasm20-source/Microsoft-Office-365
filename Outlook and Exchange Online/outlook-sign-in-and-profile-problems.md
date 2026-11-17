
# ☁️ Outlook Sign-In and Profile Troubleshooting

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Troubleshoot common Microsoft Outlook problems, sign-in failures, Outlook using the wrong account, and profile errors at startup. Sign-in problems are among the most frequent Outlook tickets for an IT Help Desk Tier 1 and Tier 2 technician, and most of them come from the account, the licence or stale saved credentials, not from Outlook itself.

---

## 💡 Where Can the Problem Be?

| Layer | Examples |
|-------|----------|
| **The account** | Wrong password, expired password, blocked sign-in, locked account |
| **The licence** | No licence that includes Exchange Online |
| **Multi-factor authentication** | The approval fails or times out |
| **Saved credentials** | Old or damaged sign-in data on the computer |
| **The profile** | A damaged or misconfigured Outlook profile |

> **First question:** can the user sign in at **Outlook on the web** (`outlook.office.com`)? If yes, the account and the licence are fine, and the problem is on the computer. If not, check the account and the licence.

### Prerequisites

- Access to the affected Windows computer
- Access to the Microsoft 365 Admin Center, if you have to check the account
- Permission to manage Outlook profiles and saved credentials

---

## 🔧 Issue 1 - Outlook Sign-In Problems

### Steps

1. **Verify the credentials.** Confirm the user enters the correct **work or school account** and password, not a personal Microsoft account.
2. **Check the sign-in status.** Open the [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Users → Active users** → select the user. Check that sign-     in is **not blocked**, and that the account is not locked and the password has not expired.
3. **Check the licence.** Open the **Licenses and apps** tab and confirm that a licence that includes Exchange Online is assigned.


 **Screenshots: account and licence checks:**


<img width="1920" height="1080" alt="Active users list with the user selected" src="https://github.com/user-attachments/assets/c36a9afb-2b77-4f4f-b5cb-9d3ebff12af5" />


<img width="1920" height="1080" alt="The user's Licenses and apps tab" src="https://github.com/user-attachments/assets/930b278e-4429-403f-9b62-8016266d42ef" />


2. **Clear the saved credentials, if needed:**
   1. Close Outlook and the other Office applications.
   2. Open **Control Panel → Credential Manager → Windows Credentials**.
   3. Find the Microsoft Office or Outlook entries for the **affected account** and remove only those.
   4. Open Outlook and sign in again.


 **Screenshots: Credentials manager:**



<img width="1920" height="1080" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/2a8ac170-5c44-4cf8-aa28-48fb9248ab87" />


<img width="1920" height="1080" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/31018a05-c8f4-4dc3-8405-002ce58101b4" />


<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/9954a83e-6363-48ea-aad9-01172ed091e9" />

<img width="1920" height="1080" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/2ed3f24d-04ca-4753-88ef-62f4fae98a17" />

**Expected result:** Outlook signs in successfully, if the cause was a wrong password, a blocked account, a missing licence or stale saved credentials.

> **Caution:** Remove only the entries for the affected account. Removing other credentials can sign the user out of other apps. The user may also need to approve multi-factor authentication again.

---

## 🔧 Issue 2 - Outlook Uses the Wrong Account

### Steps

1. Open Outlook.
2. Go to **File → Office Account**.
3. Select **Sign out**, if it is available.
4. Sign in with the correct work or school account.
5. Check the account shown in Outlook.

**Screenshots: switching the account:**


<img width="1920" height="1080" alt="Credential Manager Windows Credentials with the Microsoft Office entries" src="https://github.com/user-attachments/assets/c9d6dfaf-74b5-43ec-bd04-63b38a485104" />

<img width="1920" height="1080" alt="Removing a saved credential for the affected account" src="https://github.com/user-attachments/assets/45b66c9a-6637-495f-87b8-38a63239852f" />



**Expected result:** Outlook uses the intended account.

> **Notes:**
> - Signing out of the Office account signs the user out of **all** Office apps on that computer, not only Outlook.
> - In some Outlook versions, switching the account is done in the Outlook settings or in **Windows Settings → Accounts → Access work or school**, not on the Office Account page.

---

## 🔧 Issue 3 - Outlook Profile Errors on Launch

If Outlook shows a profile error at startup, create a new profile. The steps are in the [Corrupted Outlook Profile](./outlook-corrupted-profile.md) file. In short:

1. Close Outlook.
2. Open **Control Panel → Mail (Microsoft Outlook) → Show Profiles**.
3. Write down the name of the existing profile.
4. Click **Add**, enter a name for the new profile, and add the email account.
5. Under **When starting Microsoft Outlook, use**, select the new profile, or **Prompt for a profile to be used**.
6. Click **Apply → OK**, then start Outlook and test.

**Screenshots: Control Panel:**

<img width="1920" height="1080" alt="Control Panel Mail window with Show Profiles" src="https://github.com/user-attachments/assets/3e631f65-bf00-4642-b85c-2687e39abbe6" />

<img width="1920" height="1080" alt="Mail Profiles window with the Add button" src="https://github.com/user-attachments/assets/813a8eb5-60ee-4b37-b83f-6185fc668d64" />

<img width="1920" height="1080" alt="Entering the new profile name" src="https://github.com/user-attachments/assets/53d803d8-908f-400b-9d9a-181ff6551a2e" />

<img width="1920" height="1080" alt="Setting up the email account in the new profile" src="https://github.com/user-attachments/assets/30705870-3399-4a10-bd2e-f3a4c7863300" />

<img width="1920" height="1080" alt="Selecting the new profile as the default" src="https://github.com/user-attachments/assets/c868f619-dda4-495e-8fbf-47526547f7e2" />

<img width="1920" height="1080" alt="Outlook open with the new profile" src="https://github.com/user-attachments/assets/f9351464-e500-4aa4-91b2-0778f4fd9559" />

**Expected result:** Outlook opens with the new profile, if the old profile was damaged or set up wrongly.

> **Note:** Creating a new profile does not delete the old one. Keep it until the new profile works.

---

## ✅ Verification Checklist

- [ ] Outlook signs in without errors
- [ ] The correct account is shown
- [ ] The mailbox loads
- [ ] Outlook opens without profile errors

---

## 🛠️ Common Problems

| Symptom | Likely cause | What to check |
|---------|--------------|---------------|
| **Outlook keeps asking for the password** | Stale credentials, an expired password, or a multi-factor authentication problem | Credential Manager, the password status, the authenticator app |
| **"Your account has been blocked"** | Sign-in is blocked | Admin Center → the user → sign-in status |
| **Works in Outlook on the web, not in Outlook** | Saved credentials or the profile | Issue 1 (credentials), then Issue 3 (profile) |
| **Outlook shows the wrong mailbox** | The wrong account is signed in | Issue 2 |
| **Sign-in fails and the date or time is wrong** | The computer's clock is out of sync | Correct the date, time and time zone, then sign in again |
| **Error at startup about the profile** | A damaged profile | Issue 3, or see [Corrupted Outlook Profile](./outlook-corrupted-profile.md) |

---

## 🔗 Related Topics

| Topic | File |
|-------|------|
| **Corrupted Outlook profile** | [Corrupted Outlook Profile](./outlook-corrupted-profile.md) |
| **Cannot send or receive email** | [Outlook Troubleshooting - Cannot Send or Receive Emails](./outlook-cannot-send-receive.md) |
| **Reset password and block sign-in** | [Reset Password and Block Sign-In](./reset-password-block-signin.md) |

---

## 💡 Next Step

→ [Cannot Send and Receive Emails](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/cannot-send-and-receive-emails.md)


























