
# ☁️ Outlook Troubleshooting - Cannot Send or Receive Emails

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Diagnose and fix common Outlook email delivery problems, messages stuck in the Outbox, no new mail arriving, and bounced emails. The steps go from the simplest check (the connection) to the Microsoft 365 service and the mailbox, so you find the cause before you change anything.

---

## 💡 Where can the Issue been caused ?

| Layer | Examples |
|-------|----------|
| **The connection** | No internet, or Outlook is in offline mode |
| **Outlook** | A stuck message, a damaged profile, or an add-in |
| **The mailbox** | The mailbox is full, or a message is too large |
| **Microsoft 365** | An Exchange Online outage or incident |
| **The message** | A wrong address, or the recipient's server rejects it (a bounce) |

> **First question:** does the same mailbox work in **Outlook on the web** (`outlook.office.com`)? If it does, the mailbox and the service are fine, and the problem is in the Outlook desktop app or the computer. If it fails there too, check the mailbox and the Microsoft 365 service.

| Setting | Value |
|---------|-------|
| **Tools** | Outlook, Outlook on the web, Microsoft 365 Admin Center |
| **Where to check the service** | Admin Center → **Health → Service health** |

---

## 🔧 Part 1 - Diagnose Send and Receive Problems

1. **Check the Outbox.** Open Outlook and look for messages stuck in the **Outbox** folder.
2. **Check offline mode.** The status bar at the bottom of Outlook shows **Working Offline** or **Disconnected** when Outlook is not connected. On the **Send / Receive** tab, check the **Work Offline** button. If it is highlighted, click it **once** to go back online.
3. **Check the internet connection.** Confirm the user can open websites.
4. **Check the Microsoft 365 service health.** Open the [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Health → Service health**. Without admin access, ask an administrator to check.
5. **Send a test email** to the user's own address, and check that it arrives.
6. **Compare with webmail.** If your policy allows it, test the same mailbox in Outlook on the web, to see whether only the desktop app is affected.

> **Note:** The new Outlook for Windows has no **Work Offline** button. It shows a connection message instead.

**Expected result:** The cause is narrowed down to the connection, Outlook, the mailbox, the Microsoft 365 service or the message.

---

## 🔧 Part 2 - Check Microsoft 365 Service Health

If many users cannot send or receive mail, the cause may be a Microsoft outage and not a local problem.

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com) with an administrator account.
2. Go to **Health → Service health**.
3. Check the status of:
   - **Exchange Online**, which provides the hosted email
   - **Microsoft 365 suite**, for wider incidents that can affect users
4. Look for incidents or advisories that affect email.
5. Select the incident and read its **advisory ID** (Exchange Online incidents usually start with `EX`, for example `EX123456`, an example only), the affected services, the user impact and Microsoft's latest update.
6. Follow any recommended actions, and watch the incident for updates.
7. If Microsoft confirms an outage, tell the affected users and follow your organisation's escalation process. Do not change settings on individual computers.

**Screenshot: Service health:**

<img width="1920" height="1080" alt="Microsoft 365 Admin Center Service health page showing the status of Exchange Online" src="https://github.com/user-attachments/assets/6b8095b4-0f28-4ce1-bc6e-0dd1ea861954" />

**Expected result:** You know whether the problem is a reported Microsoft 365 incident, or needs local troubleshooting.

---

## 🔧 Part 3 - Fix Messages Stuck in the Outbox

| Step | What to do |
|:----:|------------|
| 1 | Make sure Outlook is **online**, then press **F9** (**Send / Receive All Folders**) |
| 2 | Open the stuck message, and check the **recipient address** and the **attachments**. A very large attachment can block the Outbox |
| 3 | If the message is too large, move it to **Drafts** (drag it out of the Outbox), shrink or remove the attachment, or share the file with a **OneDrive link**, and send again |
| 4 | Check that the **mailbox is not full**: **File → Info** shows the mailbox size. Delete old items and empty **Deleted Items** if it is close to the limit |
| 5 | Start Outlook in **safe mode** to rule out an add-in: press **Win + R**, type `outlook.exe /safe` and press **Enter** |
| 6 | If it works in safe mode, turn off add-ins one at a time (**File → Options → Add-ins**) |
| 7 | If the problem continues, restart Outlook and the computer, and repair the Outlook profile or create a new one, following your organisation's procedure |

> Do not delete a stuck message that the user still needs. Move it to **Drafts** first.

---





## ✅ Verification

- [ ] Outlook is connected and not in offline mode
- [ ] The internet connection works
- [ ] The Microsoft 365 service health has been checked
- [ ] A test email is delivered to the user's own address
- [ ] No unexpected messages remain in the Outbox
- [ ] The user can send and receive mail normally

---

## 🛠️ Common Problems

| Symptom | Likely cause | What to check |
|---------|--------------|---------------|
| **Messages stay in the Outbox** | Offline mode, a large attachment, or no connection | Offline mode, the attachment size, the internet connection |
| **Outlook shows "Disconnected" or "Trying to connect"** | No connection, or a problem with the account | The internet connection, service health, the webmail test |
| **Nothing new arrives, but sending works** | A rule, a full mailbox, or a filter | The mailbox size, **Rules**, the **Junk Email** folder |
| **Everyone has the problem** | A Microsoft 365 incident | Admin Center → Service health |
| **It works in webmail, but not in Outlook** | The profile, an add-in or the cache | Safe mode, a new profile |
| **A message bounces** | A wrong address, a full mailbox or a block | The NDR code and text |

---

## 💡 Next Step

→ [Sync Issues – Mail Not Updating](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/sync-issues-mail-not-updating.md)







































