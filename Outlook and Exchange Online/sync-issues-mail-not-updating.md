# ☁️ Outlook Troubleshooting - Sync Issues and Mail Not Updating

[ Back to Overview] → [README.md](./README.md)

---

## 📋 Summary

Troubleshoot Outlook synchronisation problems: emails that do not update, folders that do not sync, and calendar changes that do not appear. Sync tickets are common, and the first job is to find out whether the problem is in the **Outlook app on the computer**, in the **connection** or in the **mailbox and the Microsoft 365 service**.

---

## 💡 How Outlook Syncs

For a Microsoft 365 mailbox, Outlook keeps a local copy of the mailbox, called the **cache** (an OST file), and keeps it in step with Exchange Online. If the connection drops, the cache is damaged, or the service has a problem, the copy on the computer falls behind, and the user sees old mail or missing calendar entries.

| Setting | Value |
|---------|-------|
| **Client** | Classic Outlook for Windows |
| **Mail service** | Exchange Online (Microsoft 365) |
| **Local cache** | OST file, used when **Cached Exchange Mode** is on |
| **Reference check** | Outlook on the web (`outlook.office.com`) |

> **First question:** does the same mailbox show the new mail and the calendar change in **Outlook on the web**? If yes, the mailbox is up to date, and the problem is the Outlook app or the connection. If not, check the sender, the service health and the mailbox itself.

---

## 🔧 Issue 1 - Fix Email Synchronisation Problems

### Steps

1. **Sync the folders by hand.** In classic Outlook, go to **Send / Receive → Send/Receive All Folders**, or press **F9**.
2. **Check the connection status.** Hold **Ctrl** and **right-click** the Outlook icon in the notification area (near the clock). Select **Connection Status**, if it is available. The **Status** column should show **Connected**.
3. **Check the status bar.** At the bottom of Outlook, look for **Connected**, **Disconnected**, **Trying to connect** or **Working Offline**. If it shows offline, go to **Send / Receive** and check that **Work Offline** is not highlighted.
4. **Restart Outlook.** Close it completely, open it again, and check whether new messages appear.
5. **Check for filters and folders.** Make sure no **filter** is applied to the view (the status bar shows **Filter applied**), and look in the **Junk Email** folder and the **Other** tab of the Focused Inbox.
6. **Check the Microsoft 365 service health.** Open the [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Health → Service health**, and check **Exchange Online**.
7. **Test Outlook on the web.** Sign in and check whether the mailbox is up to date there.
8. **Check the mailbox size.** In Outlook, **File → Info** shows the mailbox size. A full mailbox can stop new mail.
9. **Repair Microsoft 365 Apps, if needed:**
   1. Open **Windows Settings → Apps → Installed apps**.
   2. Find **Microsoft 365** or **Microsoft Office**, click **⋯** and select **Modify**.
   3. Choose **Quick Repair** and follow the prompts. If the problem continues, run **Online Repair**, which needs an internet connection and takes longer.

**Expected result:** Mail and folders synchronise correctly, after the connection, the service or the application problem is fixed.

> If Outlook still does not update, but the mailbox is correct in Outlook on the web, the local cache may be damaged. See [Corrupted Outlook Profile](./outlook-corrupted-profile.md) for rebuilding the cache and creating a new profile.

---

## 🔧 Issue 2 - Calendar Not Syncing

### Steps

1. Open classic Outlook.
2. Go to **File → Account Settings → Account Settings**.
3. Select the Microsoft 365 or Exchange account and click **Change**, if the button is available.
4. Check whether **Use Cached Exchange Mode** is turned on.
5. If you change a setting, save it and restart Outlook.
6. Compare the calendar with **Outlook on the web**, to see whether the problem is only in the desktop app or in the mailbox itself.
7. Check the calendar view: the right calendar is ticked in the folder list, and the **time zone** in **File → Options → Calendar** is correct.
8. For a **shared calendar**, check that the user still has the permission, and that the calendar appears under **Shared Calendars**.

**Expected result:** Calendar changes appear in Outlook after the sync finishes.

> **Important:** Cached Exchange Mode is recommended for Microsoft 365 and Exchange accounts in classic Outlook, so keep it on unless a technician has a reason to change it. The new Outlook for Windows does not have this setting, and the exact menu names depend on the Outlook version.

---

## ✅ Verification Checklist

- [ ] Outlook shows **Connected**
- [ ] New emails appear after a manual sync (**F9**)
- [ ] Sent and received messages are up to date
- [ ] Calendar changes appear in Outlook and on the web
- [ ] The Microsoft 365 service health has been checked
- [ ] The problem stays fixed after restarting Outlook

---

## 🛠️ Common Problems

| Symptom | Likely cause | What to check |
|---------|--------------|---------------|
| **Mail arrives in webmail, not in Outlook** | Offline mode, a connection problem or a damaged cache | The status bar, **Connection Status**, then [Corrupted Outlook Profile](./outlook-corrupted-profile.md) |
| **Nothing arrives anywhere** | A service incident, a full mailbox or a rule | Service health, the mailbox size, **Rules**, the **Junk Email** folder |
| **Some folders are not updated** | Sync is slow or a folder is damaged | **F9**, the **Sync Issues** folder (if it is shown), restart Outlook |
| **Calendar changes are missing** | The calendar is not synced, a time zone problem, or a permission change | Compare with Outlook on the web, the time zone, the permissions |
| **"Disconnected" or "Trying to connect"** | No internet, a sign-in problem or a service problem | The internet connection, [Sign-in troubleshooting](./outlook-sign-in-profile.md), service health |
| **Outlook is slow and out of date** | A large mailbox, a faulty add-in or a damaged cache | Safe mode (`outlook.exe /safe`), the cache size, a repair |

---

## 🔗 Related Topics

| Topic | File |
|-------|------|
| **Cannot send or receive email** | [Outlook Troubleshooting - Cannot Send or Receive Emails](./outlook-cannot-send-receive.md) |
| **Corrupted Outlook profile** | [Corrupted Outlook Profile](./outlook-corrupted-profile.md) |
| **Sign-in and profile problems** | [Outlook Sign-In and Profile Troubleshooting](./outlook-sign-in-profile.md) |

---

## 💡 Next Step

→ [Outlook Troubleshooting - Cannot Send or Receive Emails](./outlook-cannot-send-receive.md)




-----------




























------
# Outlook Troubleshooting - Sync Issues and Mail Not Updating



## Objective

Troubleshoot Outlook synchronisation problems, including emails not updating, folders not syncing, and calendar changes not appearing.

## Issue 1 - Fix Email Synchronisation Issues

### Troubleshooting Steps

1. **Manually sync folders:** In classic Outlook, go to **Send / Receive → Send/Receive All Folders**, or press `F9`. <Cite refs={["turn265845search0"]}/>
2. **Check connection status:** Hold `Ctrl` and click the Outlook icon in the Windows notification area. Select **Connection Status**, if available.
3. **Restart Outlook:** Close Outlook completely, reopen it, and check whether new messages appear.
4. **Check Microsoft 365 service health:** Open [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Health → Service health** and check Exchange Online.
5. **Test Outlook on the web:** Sign in to Outlook on the web and check whether the mailbox is updating.
6. **Repair Microsoft 365 Apps if needed:**
   - Open **Windows Settings → Apps → Installed apps**.
   - Find **Microsoft 365** or **Microsoft Office**.
   - Select **Modify**.
   - Choose **Quick Repair** and follow the prompts.

**Expected result:** Emails and folders synchronise correctly after the underlying connectivity, service, or application issue is resolved.

## Issue 2 - Calendar Not Syncing

### Troubleshooting Steps

1. Open classic Outlook.
2. Navigate to **File → Account Settings → Account Settings**.
3. Select the Microsoft 365 or Exchange account and click **Change**, if available.
4. Under the account's offline settings, check whether **Use Cached Exchange Mode** is enabled.
5. If you change this setting, save the changes and restart Outlook.
6. Compare the calendar with Outlook on the web to determine whether the issue affects the desktop client or the mailbox itself.

**Expected result:** Calendar updates appear in Outlook after synchronisation completes.

**Important:** Cached Exchange Mode is recommended for Microsoft 365 and Exchange accounts in classic Outlook, but it is not available in new Outlook for Windows. The exact menu options vary by Outlook version. <Cite refs={["turn265845search1"]}/>

## Verification Checklist

- [ ] Outlook shows a connected status.
- [ ] New emails appear after a manual sync.
- [ ] Sent and received messages are up to date.
- [ ] Calendar changes appear in Outlook and on the web.
- [ ] Microsoft 365 service health has been checked.
- [ ] The issue remains resolved after restarting Outlook.


