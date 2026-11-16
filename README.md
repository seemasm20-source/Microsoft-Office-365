# ☁️ Microsoft 365 Troubleshooting Portfolio

**Portfolio:** IT Help Desk Tier 1 & Tier 2 - Microsoft 365 Labs

**Platform:** Microsoft 365 (cloud)

**Purpose:** Demonstrate hands-on Microsoft 365 administration and troubleshooting skills for IT Help Desk Tier 1 and Tier 2

**Author:** Seema Soapanahalli Mallikarjunaiah

---

## 📌 About This Portfolio

This portfolio documents hands-on troubleshooting of Microsoft 365 services. It covers the most common Tier 1 and Tier 2 Help Desk tasks: managing users and licences in the Microsoft 365 Admin Center, fixing Outlook and Exchange Online problems, and troubleshooting Microsoft Teams.

Each scenario follows the same flow: summary, steps, verification, and a table of common problems.

> **Lab Note:** The scenarios were built on a Microsoft 365 tenant, with screenshots of the steps. Some files, such as the sync and service health checks, are reference guides that explain the standard method and have no screenshots.

---

## 🏗️ Environment

| Component | Detail |
|-----------|--------|
| **Platform** | Microsoft 365 (cloud) |
| **Admin portal** | `admin.microsoft.com` |
| **Directory** | Microsoft Entra ID |
| **Email** | Exchange Online with classic Outlook for Windows |
| **Collaboration** | Microsoft Teams (new Teams) |
| **Client** | Windows 11 |
| **Level** | Tier 1 & Tier 2 Help Desk |

---

## 📁 Portfolio Structure

```text
office-365/
│
├── 01-m365-admin/
│   ├── README.md
│   ├── create-manage-users.md
│   ├── assign-remove-licences.md
│   ├── reset-passwords-block-signin.md
│   └── delete-restore-user.md
│
├── 02-outlook-exchange/
│   ├── README.md
│   ├── signin-profile-problems.md
│   ├── cannot-send-receive.md
│   ├── sync-issues.md
│   └── corrupted-profile.md
│
└── 03-teams/
    ├── README.md
    ├── signin-licence-checks.md
    ├── microphone-camera-meetings.md
    ├── repair-reset-teams.md
    └── clear-teams-cache.md
```

| Section | Topic | Key Skills |
|---------|-------|------------|
| **Microsoft 365 Admin Center** | Users, licences, passwords and accounts | Create users, assign licences, reset passwords, block sign-in, delete and restore |
| **Outlook and Exchange Online** | Email client and mailbox problems | Sign-in, profiles, send and receive, sync, data files |
| **Microsoft Teams** | Collaboration app problems | Sign-in, licences, audio and video, repair, cache |

---

## ☁️ Section 1 - Microsoft 365 Admin Center

| Topic | What it covers | File |
|-------|----------------|------|
| **Create a New User** | Create a user, set a temporary password and assign a licence | [Create and Manage Users](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Microsoft%20365%20Admin%20Center/create-and-manage-users.md) |
| **Assign and Remove Licences** | Give or take away a Microsoft 365 licence | [Assign and Remove License](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Microsoft%20365%20Admin%20Center/assign-and-remove-license.md) |
| **Reset Password and Block Sign-In** | Reset a password and block or unblock sign-in | [Reset Password and Block Sign-In](./01-m365-admin/reset-passwords-block-signin.md) |
| **Delete and Restore a User** | Delete an account and restore it within 30 days | [Delete and Restore a User](./01-m365-admin/delete-restore-user.md) |

---

## 📧 Section 2 - Outlook and Exchange Online

| Topic | What it covers | File |
|-------|----------------|------|
| **Sign-In and Profile Problems** | Sign-in failures, the wrong account, saved credentials, profile errors | [Outlook Sign-In and Profile Troubleshooting](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/outlook-sign-in-and-profile-problems.md) |
| **Cannot Send or Receive Emails** | Stuck Outbox, offline mode, service health, bounced emails | [Cannot Send or Receive Emails](./02-outlook-exchange/cannot-send-receive.md) |
| **Sync Issues and Mail Not Updating** | Manual sync, connection status, calendar sync, Cached Exchange Mode | [Sync Issues](./02-outlook-exchange/sync-issues.md) |
| **Corrupted Outlook Profile** | Safe mode, add-ins, OST and PST repair, a new profile | [Corrupted Outlook Profile](./02-outlook-exchange/corrupted-profile.md) |

---

## 💬 Section 3 - Microsoft Teams

| Topic | What it covers | File |
|-------|----------------|------|
| **Sign-In and Licence Checks** | Sign-in failures, licence checks, missing teams and channels | [Sign-In and Licence Troubleshooting](./03-teams/signin-licence-checks.md) |
| **Microphone, Camera and Meetings** | Device settings, Windows permissions, meeting restrictions | [Microphone, Camera and Meeting Troubleshooting](./03-teams/microphone-camera-meetings.md) |
| **Repair, Reset and Reinstall** | Fixing the Teams app, from the least to the most disruptive fix | [Repair, Reset and Reinstall](./03-teams/repair-reset-teams.md) |
| **Clear the Teams Cache** | Fixing slow or frozen Teams by clearing the cache | [Teams Cache Clearing](./03-teams/clear-teams-cache.md) |

---

## 🎯 Microsoft 365 Troubleshooting Matrix

| Ticket | Likely causes | What to check |
|--------|---------------|---------------|
| **A new employee needs an account** | No account yet | Create the user, set a temporary password and assign a licence |
| **"I can't use Teams or email" after account creation** | No licence assigned, or the location is missing | **Licenses and apps**, and the usage location |
| **"I forgot my password"** | Forgotten or expired password | Verify the caller, then reset the password |
| **Block an account immediately** | A leaver or a compromised account | Block sign-in, and sign the user out of all sessions |
| **A user was deleted by mistake** | An accidental deletion | **Deleted users**, restore within 30 days, then assign a licence |
| **Outlook keeps asking for the password** | Stale credentials, an expired password or MFA | Credential Manager, the account status |
| **Outlook shows the wrong account** | The wrong account is signed in | **File → Office Account**, sign out and in |
| **Messages stuck in the Outbox** | Offline mode, a large attachment or no connection | The status bar, the attachment, **F9** |
| **Email bounces back** | A wrong address, a full mailbox or a block | The error code in the report |
| **Mail is not updating in Outlook** | A connection problem or a damaged cache | **Connection Status**, webmail test, then the cache |
| **Outlook crashes or will not start** | An add-in, a damaged profile or a data file | Safe mode (`outlook.exe /safe`), then a new profile |
| **Teams will not sign in** | The account, the licence or the app | Web version, **Licenses and apps**, service health |
| **Teams shows no teams or channels** | Not a member, or a new licence | Team membership, then sign out and in |
| **Others cannot hear me in Teams** | The wrong microphone, a permission or a meeting setting | Teams device settings, Windows privacy settings |
| **Teams is slow or freezes** | A damaged cache or a damaged app | Clear the cache, then Repair, then Reset |

---

## 📋 Key Locations and Commands

| Item | Where or how |
|------|--------------|
| **Admin Center** | `admin.microsoft.com` → **Users → Active users** |
| **Service health** | Admin Center → **Health → Service health** |
| **Outlook safe mode** | **Win + R** → `outlook.exe /safe` |
| **Outlook profiles** | Control Panel → **Mail (Microsoft Outlook) → Show Profiles** |
| **Outlook cache folder** | `%localappdata%\Microsoft\Outlook` |
| **Saved credentials** | Control Panel → **Credential Manager → Windows Credentials** |
| **Teams cache folder** | `%localappdata%\Packages\MSTeams_8wekyb3d8bbwe\LocalCache\Microsoft\MSTeams` |
| **Repair or reset an app** | Windows **Settings → Apps → Installed apps → ⋯ → Advanced options** |
| **Outlook on the web** | `outlook.office.com`, to test a mailbox |
| **Teams on the web** | `teams.microsoft.com`, to test an account |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Microsoft 365 Admin Center | User, licence and password management |
| Microsoft Outlook | Email client troubleshooting |
| Outlook on the web and Teams on the web | Testing the account and the mailbox without the desktop app |
| Control Panel → Mail | Outlook profile management |
| Inbox Repair Tool (`SCANPST.EXE`) | Repairing PST data files |
| Credential Manager | Saved credentials |
| Microsoft Teams | Teams troubleshooting |
| Windows Settings → Apps | Repair and reset of applications |
| PowerShell | Clearing the Teams cache |
| Microsoft 365 Service Health | Checking for Microsoft outages |

---

## 📚 Skills Demonstrated

### Microsoft 365 Admin Center
- Create and manage user accounts
- Assign and remove Microsoft 365 licences
- Reset passwords and block sign-in
- Delete and restore user accounts

### Outlook and Exchange Online
- Troubleshoot Outlook sign-in and profile problems
- Fix cannot send and receive email problems, including bounced messages
- Resolve sync problems and mail that is not updating
- Fix a corrupted Outlook profile: safe mode, rebuilding the OST cache, repairing PST files with the Inbox Repair Tool, and creating a new profile

### Microsoft Teams
- Diagnose sign-in problems and licence issues
- Troubleshoot microphone, camera and meeting problems
- Repair, reset and reinstall the Teams app
- Clear the Teams cache to fix performance problems

### General
- Checking Microsoft 365 service health before changing a computer
- Testing in the web version to separate account problems from app problems
- Following the order of fixes from the least to the most disruptive
- Technical documentation for a GitHub portfolio

---

## 🎯 Real-World Help Desk Tickets

| Caller Complaint | Root Cause | Fix Applied |
|------------------|------------|-------------|
| "I can't sign in to Outlook" | A wrong or expired password, a blocked account, or stale credentials | Checked the account and the licence, cleared the saved credentials |
| "My email is stuck in the Outbox" | Offline mode or a large attachment | Went back online, moved the message to Drafts, shared a link |
| "Outlook won't open" | An add-in or a damaged profile | Safe mode, turned off add-ins, created a new profile |
| "I can't use Teams" | No licence, or the account | Assigned a licence that includes Teams |
| "People can't hear me in Teams" | The wrong device or a privacy permission | Selected the right microphone, checked the Windows permission |
| "Teams is slow" | A damaged cache | Cleared the cache, then Repair and Reset if needed |

---

## 🔗 Related Portfolios

| Portfolio | Link |
|-----------|------|
| **Windows Server on Azure** | [Windows Server on Azure](https://github.com/seemasm20-source/Windows-Server-Azure-AD) |
| **Networking Labs** | [Networking Labs](https://github.com/seemasm20-source/networking-labs) |

---

## 🎓 Learning Outcome

This portfolio provided hands-on experience with the Microsoft 365 Admin Center, Outlook and Teams. It built practical skills for common help desk tickets: finding out whether a problem is in the account, the licence, the app or the Microsoft service, and choosing the least disruptive fix. These skills are relevant to IT Help Desk Tier 1 and Tier 2 roles.

---

## ✅ Conclusion

User management, licences, password resets and account recovery were documented in the Microsoft 365 Admin Center. Outlook sign-in, send and receive, sync and profile problems, and Teams sign-in, audio and video, repair and cache problems, were diagnosed and fixed.

Together these show a systematic approach to Microsoft 365 support: confirm the symptom, test in the web version, check the account, the licence and the service health, and then fix the app, starting with the least disruptive step.

> **Note:** This portfolio is actively being built. Labs and screenshots are added as each section is completed.
