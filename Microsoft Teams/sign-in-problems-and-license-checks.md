# ☁️ Microsoft Teams - Sign-in and Licence Troubleshooting

[ Back to Overview] → [README.md](./README.md)

---

## 📋 Summary

Troubleshoot Microsoft Teams sign-in failures, licence problems and missing teams or channels. For most of these tickets, the cause is the account, the licence or the team membership, not the Teams app itself, so check those before you reinstall anything.

---

## 💡 Where Can the Problem Be?

| Symptom | Likely area | First check |
|---------|-------------|-------------|
| **Cannot sign in to Teams** | The account, the password, the sign-in status, or the Teams app | Can the user sign in at `teams.microsoft.com`? |
| **Teams opens but shows an error about a missing licence** | The licence | Admin Center → **Licenses and apps** |
| **Teams opens but shows no teams or channels** | Team membership, or the licence is new | Is the user a member of the team? |

> **First question:** does the web version of Teams work? If it does, the account and the licence are fine, and the problem is in the desktop app. If it fails too, the problem is the account, the licence or a Microsoft service problem.

| Setting | Value |
|---------|-------|
| **Tools** | Microsoft 365 Admin Center (`admin.microsoft.com`) and Teams on the web (`teams.microsoft.com`) |
| **Where to check the licence** | Users → Active users → the user → **Licenses and apps** |
| **Where to check service health** | Admin Center → **Health → Service health** |

---

## 🔧 Part 1 - Diagnose Sign-in Problems

### Step 1 - Verify the Account

Confirm that the user signs in with the correct **work or school account**, not a personal Microsoft account. Ask whether the user can sign in to [Teams on the web](https://teams.microsoft.com).

### Step 2 - Check the Licence

1. Open the [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Go to **Users → Active users** and select the user.
3. Open the **Licenses and apps** tab.
4. Check that a licence that includes Teams is assigned, and that **Microsoft Teams** is turned on in the licence's apps list.

**Screenshot: licence check:**

<img width="1920" height="1080" alt="The user's Licenses and apps tab with a licence that includes Microsoft Teams" src="https://github.com/user-attachments/assets/b9e32f7d-6664-4e92-b507-27f1f7442b0e" />

### Step 3 - Check the Sign-in Status

In the user's panel, check that sign-in is **not blocked**, and that the account is not locked or has an expired password.

### Step 4 - Check Service Health

In the Admin Center, go to **Health → Service health** and look for Microsoft Teams incidents. If there is an incident, wait for Microsoft to fix it, and tell the user.

---

## 🔧 Part 2 - Fix: Cannot Sign In to Teams

1. Sign out of Teams, if possible.
2. Quit Teams completely (the system tray icon → **Quit**) and open it again.
3. Sign in again with the correct work or school account.
4. If the problem continues, clear the Teams cache. See [Teams Cache Clearing](./teams-cache-clearing.md).
5. Test Teams on the web, to see whether the problem is only in the desktop app.
6. If only the desktop app fails, use [Teams Repair, Reset and Reinstall](./teams-repair-reset-reinstall.md).

> **Note:** Clearing the cache can help with problems in the app, but it does not fix every sign-in failure. Do not delete saved credentials or cached data without a reason.

**Screenshot: Teams sign-in:**

<img width="1920" height="1080" alt="Microsoft Teams sign-in screen" src="https://github.com/user-attachments/assets/76621ebd-ea57-41a8-89c2-0178e2ac6041" />

### Common Sign-in Causes

| Cause | What to check |
|-------|---------------|
| **Wrong account** | The user signs in with a personal account instead of the work account |
| **Expired or wrong password** | Reset the password. See [Reset Password and Block Sign-In](./reset-password-block-signin.md) |
| **Sign-in is blocked** | Unblock it in the user's panel |
| **Multi-factor authentication problem** | The phone, the authenticator app and the time on the device |
| **Missing licence** | Assign a licence that includes Teams |
| **Wrong organisation** | A user who belongs to several organisations signs in to the wrong one, and must switch organisation in Teams |
| **A blocking policy** | A sign-in policy (such as conditional access) blocks the sign-in. Ask an administrator to check the sign-in logs |

---

## 🔧 Part 3 - Fix: Teams Opens but Shows No Teams or Channels

1. In the Admin Center, check that the user has a licence that includes Teams.
2. If the licence was assigned recently, give it time to provision and check again. This can take up to 24 hours in some cases, but it is not guaranteed.
3. Ask the user to sign out of Teams and sign in again.
4. Check that the user has been **added to the team**, and has access to the channel. If not, ask a **team owner** to add the user.
5. If the problem continues, check the Teams service health, and escalate to the next support level.

> **Important:** A Teams licence does not add a user to any team. Team membership is separate, and it is set by the team owners or by an administrator.

### Why Are the Teams Missing?

| Cause | What to check |
|-------|---------------|
| **The user is not in the team** | Ask a team owner to add the user |
| **The licence is new** | Wait, then ask the user to sign out and in |
| **The team is hidden or archived** | In Teams, open **Manage teams** and check for hidden or archived teams |
| **The channel is private** | A private channel needs separate membership |
| **The user is in the wrong organisation** | Switch organisation in Teams |
| **The app is not up to date** | Restart Teams, or check the web version |

---

## ✅ Verification

- [ ] The user can sign in to Teams
- [ ] Teams opens without the original error
- [ ] The expected teams and channels are visible
- [ ] The user can open the required team or channel
- [ ] The issue is resolved, or documented for escalation

---

## 💡 Next Step

→ [Teams Microphone, Camera and Meeting Troubleshooting](./teams-audio-camera.md)































-----------------------


# Microsoft Teams Sign-in and Licence Troubleshooting


## Objective

Troubleshoot Microsoft Teams sign-in failures, licence issues and missing teams or channels.

## 1. Diagnose Sign-in Problems

1. **Verify the account:** Confirm the user is signing in with the correct work or school account. Ask whether they can sign in to [Teams on the web](https://teams.microsoft.com).
2. **Check the licence:** Open [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Users → Active users → select the user → Licences and apps**. Verify that a Teams licence or an appropriate licence that includes Teams is assigned.
3. **Check sign-in status:** In the user's account settings, confirm that sign-in is not blocked.
4. **Check service health:** In Admin Center, go to **Health → Service health** and check for Microsoft Teams incidents.

## 2. Fix  Cannot Sign In to Teams

1. Sign out of Teams, if possible.
2. Completely quit Teams and reopen it.
3. Sign in again using the correct work or school account.
4. If the issue persists, clear the Teams cache using the procedure for the installed Teams version.
5. Test Teams on the web to help determine whether the problem is limited to the desktop app.

**Note:** Clearing the cache may help with local app issues, but it does not resolve every sign-in failure. Do not delete credentials or cached data unnecessarily.

## 3. Fix  Teams Opens but Shows No Teams or Channels

1. In Microsoft 365 Admin Center, confirm the user has an appropriate Teams licence.
2. If the licence was assigned recently, allow time for provisioning and check again. It may take up to 24 hours in some cases, but this is not guaranteed.
3. Ask the user to sign out and sign back in.
4. Confirm that the user has been added to the relevant team and has the required access.
5. If the issue persists, check Microsoft Teams service health and escalate when necessary.

**Important:** A Teams licence alone does not automatically add a user to every team or channel.

## 4. Verification

- [ ] User can sign in to Teams.
- [ ] Teams opens without the original error.
- [ ] The expected teams and channels are visible.
- [ ] The user can access the required team or channel.
- [ ] The issue is resolved or documented for escalation.












**<img width="1920" height="1080" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/76621ebd-ea57-41a8-89c2-0178e2ac6041" />**





















<img width="1920" height="1080" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/b9e32f7d-6664-4e92-b507-27f1f7442b0e" />




























