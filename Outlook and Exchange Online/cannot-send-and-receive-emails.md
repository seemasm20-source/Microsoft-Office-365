
# Outlook Troubleshooting - Cannot Send or Receive Emails


Diagnose and resolve common Outlook email delivery issues, including messages stuck in the Outbox and bounced emails.

## Issue 1 - Diagnose Send/Receive Problems

### Troubleshooting Steps

1. **Check the Outbox:** Open Outlook and check whether messages are stuck in the Outbox.
2. **Check Offline mode:** Open the **Send / Receive** tab and verify that **Work Offline** is disabled,toggling ON will work.
3. **Check internet connectivity:** Confirm the user can access websites.
4. **Check Microsoft 365 service health:** Open [Microsoft 365 Admin Center](https://admin.microsoft.com) → **Health → Service health**.
5. **Send a test email:** Send a test message to the user's own email address and check whether it arrives.
6. **Compare Outlook with webmail:** If permitted, test Outlook on the web to determine whether the issue affects only the desktop application.

**Expected result:** The cause is narrowed down to connectivity, Outlook configuration, Microsoft 365 service availability, or email delivery.

## Issue 2 - Check Microsoft 365 Service Health

### Problem

Users cannot send or receive emails in Outlook, and the issue may be caused by a Microsoft 365 service outage rather than a local computer or Outlook configuration problem.

### Troubleshooting Steps

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com) using an administrator account.
2. Navigate to **Health → Service health**.
3. Check the status of:
   - **Exchange Online** — responsible for hosted email services.
   - **Microsoft 365 suite** — check for broader service incidents that may affect users.
4. Look for service incidents or advisories affecting email.
5. Select the relevant incident to review its advisory ID, such as `EX123456` (example only), affected services, user impact, and Microsoft's latest updates.
6. Follow the recommended actions, if any, and monitor the incident for updates.
7. If Microsoft confirms an outage, inform affected users and follow your organisation's escalation process instead of making unnecessary changes to individual computers.



### Expected Result

Determine whether the email issue is related to a reported Microsoft 365 service problem or requires further local troubleshooting.



## Verification Checklist

* [ ] Outlook is connected and not in Work Offline mode.
* [ ] Internet connectivity is working.
* [ ] Microsoft 365 service health has been checked.
* [ ] Test email delivery has been verified.
* [ ] No unexpected messages remain stuck in the Outbox.













<img width="1920" height="1080" alt="Screenshot (151)" src="https://github.com/user-attachments/assets/6b8095b4-0f28-4ce1-bc6e-0dd1ea861954" />




