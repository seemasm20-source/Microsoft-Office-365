# Troubleshooting - Corrupted Outlook Profile



## Objective

Troubleshoot Outlook crashes, connection problems, missing emails, and profile-related errors using Safe Mode, data-file repair, and a new Outlook profile.

## Signs of a Corrupted Profile

Common symptoms include:

- Outlook crashes or closes during startup.
- Outlook cannot connect to Exchange.
- Emails do not load despite a working internet connection.
- Error: `Cannot start Microsoft Outlook`.
- Error: `The set of folders cannot be opened`.

**Note:** These symptoms can also be caused by add-ins, data-file issues, authentication failures, or Microsoft 365 service problems.

## Fix 1 - Start Outlook in Safe Mode

### Steps

1. Close Outlook.
2. Press `Windows + R`.
3. Type `outlook.exe /safe` and press **Enter**.
4. If Outlook opens successfully, an add-in or customisation may be causing the problem.
5. In classic Outlook, navigate to **File → Options → Add-ins**.
6. Under **Manage**, select **COM Add-ins**, then click **Go**.
7. Untick the add-ins and click **OK**.
8. Restart Outlook normally.
9. If Outlook works, re-enable add-ins one at a time to identify the problematic one.

**Expected result:** Outlook opens normally after the problematic add-in is disabled.

*Note: Safe Mode and COM Add-ins steps apply to classic Outlook for Windows, not necessarily the new Outlook app.*



## Fix 2  - Create a New Outlook Profile

### Steps

1. Close Outlook.
2. Open **Control Panel**.
3. Search for and open **Mail (Microsoft Outlook)**.
4. Click **Show Profiles**.
5. Note the existing profile name.
6. Click **Add** and enter a name for the new profile.
7. Follow the prompts to configure the email account.
8. Under **When starting Microsoft Outlook, use**, select the new profile as the default.
9. Click **Apply → OK**.
10. Restart Outlook and test the new profile.

[Click here to view Outlook Sign-in and Profile Troubleshooting](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/outlook-sign-in-and-profile-problems.md)


**Expected result:** Outlook works with the new profile if the previous profile was damaged or misconfigured.

**Note:** Keep the old profile until the new one has been tested successfully.

## Verification Checklist

- [ ] Outlook opens without crashing.
- [ ] The mailbox loads correctly.
- [ ] Emails can be sent and received.
- [ ] Outlook connects to Exchange or Microsoft 365.
- [ ] The issue does not return after restarting Outlook.






<img width="1920" height="1080" alt="Screenshot (139)" src="https://github.com/user-attachments/assets/fe9856ec-54ae-44e5-91a8-8b506b8a8334" />

























<img width="1920" height="1080" alt="Screenshot (140)" src="https://github.com/user-attachments/assets/50b1cfcb-f0f0-498c-a131-18533ce0579a" />


























<img width="1920" height="1080" alt="Screenshot (141)" src="https://github.com/user-attachments/assets/13add100-968a-43c1-98a3-94d2e7b8aab4" />

























<img width="1920" height="1080" alt="Screenshot (142)" src="https://github.com/user-attachments/assets/22683fdf-fcd6-40da-8fe3-00649b2e7e56" />



























<img width="1920" height="1080" alt="Screenshot (143)" src="https://github.com/user-attachments/assets/331a491c-d304-4d25-9540-a8f3ec40ac4b" />
































<img width="1920" height="1080" alt="Screenshot (144)" src="https://github.com/user-attachments/assets/0dc27c56-f0d6-4291-aff3-943c5394ab39" />

















<img width="1920" height="1080" alt="Screenshot (145)" src="https://github.com/user-attachments/assets/d0de2a56-eb0d-4d11-a730-8bed07148ea2" />























