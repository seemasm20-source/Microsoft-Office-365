
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

## Issue 2 — Calendar Not Syncing

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

## Troubleshooting Notes

- **Outlook on the web works, desktop Outlook does not:** Investigate the local Outlook application, profile, or cache.
- **Both Outlook and webmail are affected:** Check account status, mailbox availability, and Microsoft 365 service health.
- **Only the calendar is affected:** Check calendar permissions, shared-calendar behaviour, and whether the affected calendar is shared or delegated.
- **Sync is still failing:** Check Outlook's sync errors and consider further profile or cache troubleshooting before rebuilding local data.

## Key Learning

Start with a manual sync, check connection status, and compare desktop Outlook with Outlook on the web. This helps identify whether the issue is local to the application or related to the mailbox or service.
