# ☁️ Troubleshooting - Corrupted Outlook Profile

[ Back to Overview] → [README.md](./README.md)

---

## 📋 Summary

Troubleshoot Outlook crashes, connection problems, missing emails and profile errors, using Safe Mode, a data-file repair and a new Outlook profile. The fixes go from the least to the most disruptive, so the user loses as little as possible.

---

## 💡 What is an Outlook Profile?

An Outlook profile stores the email account settings and points to the **data files** that hold the mail. For a Microsoft 365 mailbox, Outlook keeps a local cache of the mailbox in an **OST** file, and the mail itself is stored in Exchange Online. A damaged profile or data file can make Outlook crash, fail to connect or show missing items, even though the mailbox is fine.

| Setting | Value |
|---------|-------|
| **Client** | Classic Outlook for Windows |
| **Profile tool** | Control Panel → **Mail (Microsoft Outlook)** |
| **Data files** | OST (a cache of the Exchange mailbox) and PST (a local archive file, if used) |
| **OST location** | `%localappdata%\Microsoft\Outlook` |

> **Check first:** does the same mailbox work in Outlook on the web (`outlook.office.com`)? If it does, the mailbox is fine, and the problem is on the computer.

### Signs of a Corrupted Profile

- Outlook crashes or closes during startup
- Outlook cannot connect to Exchange
- Emails do not load although the internet connection works
- Error: `Cannot start Microsoft Outlook`
- Error: `The set of folders cannot be opened`

> These symptoms can also come from add-ins, data-file problems, sign-in failures or a Microsoft 365 service problem. Check [Service health](https://admin.microsoft.com) before you change the profile.

---

## 🔧 Fix 1 - Start Outlook in Safe Mode

1. Close Outlook.
2. Press **Windows + R**.
3. Type `outlook.exe /safe` and press **Enter**.
4. If Outlook opens, an add-in or a customisation is probably the cause.
5. In classic Outlook, go to **File → Options → Add-ins**.
6. At **Manage**, select **COM Add-ins** and click **Go**.
7. Untick the add-ins and click **OK**.
8. Close Outlook and start it normally.
9. If Outlook works, turn the add-ins back on **one at a time** to find the one that causes the problem.

**Screenshots: Safe Mode and add-ins:**

<img width="1920" height="1080" alt="Run dialog with outlook.exe /safe entered" src="https://github.com/user-attachments/assets/fe9856ec-54ae-44e5-91a8-8b506b8a8334" />

<img width="1920" height="1080" alt="COM Add-ins window with the add-ins unticked" src="https://github.com/user-attachments/assets/50b1cfcb-f0f0-498c-a131-18533ce0579a" />


<img width="1920" height="1080" alt="Control Panel Mail window with Show Profiles" src="https://github.com/user-attachments/assets/13add100-968a-43c1-98a3-94d2e7b8aab4" />

<img width="1920" height="1080" alt="Mail Profiles window with the Add button" src="https://github.com/user-attachments/assets/22683fdf-fcd6-40da-8fe3-00649b2e7e56" />

<img width="1920" height="1080" alt="New profile name and email account setup" src="https://github.com/user-attachments/assets/331a491c-d304-4d25-9540-a8f3ec40ac4b" />

<img width="1920" height="1080" alt="Always use this profile with the new profile selected" src="https://github.com/user-attachments/assets/0dc27c56-f0d6-4291-aff3-943c5394ab39" />
**Expected result:** Outlook opens normally after the faulty add-in is turned off.

> Safe Mode and COM Add-ins apply to **classic Outlook for Windows**, not necessarily to the new Outlook app.

---



---

## 🔧 Fix 2 - Create a New Outlook Profile

1. Close Outlook.
2. Open **Control Panel** and search for **Mail (Microsoft Outlook)**.
3. Click **Show Profiles**.
4. Write down the name of the existing profile.
5. Click **Add** and enter a name for the new profile.
6. Follow the prompts to add the email account.
7. Under **When starting Microsoft Outlook, use**, select **Always use this profile** and choose the new profile.
8. Click **Apply**, then **OK**.
9. Start Outlook and test the new profile.

**Screenshots: creating the profile:**

<img width="1920" height="1080" alt="Screenshot (160)" src="https://github.com/user-attachments/assets/88bb8ab1-e792-4aa9-a511-b6dcbe6ac149" />


<img width="1920" height="1080" alt="Screenshot (161)" src="https://github.com/user-attachments/assets/794db4ac-be20-4af0-a421-35fb74949f9e" />


<img width="1920" height="1080" alt="Screenshot (162)" src="https://github.com/user-attachments/assets/112f78aa-6ec9-4bb9-b398-04a16f73b316" />


<img width="1920" height="1080" alt="Screenshot (163)" src="https://github.com/user-attachments/assets/c276ddbe-25dc-43ff-bfaf-14a5dbf75098" />


<img width="1920" height="1080" alt="Screenshot (164)" src="https://github.com/user-attachments/assets/ac2285b7-cba3-423c-b864-0e9e97a393a4" />


**Expected result:** Outlook works with the new profile, if the old profile was damaged or set up wrongly.

> **Notes:**
> - Keep the old profile until the new one has been tested.
> - A new profile starts without the old settings. Add any PST files again (**File → Open & Export → Open Outlook Data File**), and check the signatures.
> - On a managed company computer, follow your organisation's procedure for changing Outlook profiles.

---

## ✅ Verification

- [ ] Outlook opens without crashing
- [ ] The mailbox loads correctly
- [ ] Emails can be sent and received
- [ ] Outlook connects to Exchange Online (the status bar shows **Connected**)
- [ ] The problem does not return after restarting Outlook



**Screenshot: Outlook working with the new profile:**

<img width="1920" height="1080" alt="Outlook open with the mailbox loaded and connected" src="https://github.com/user-attachments/assets/d0de2a56-eb0d-4d11-a730-8bed07148ea2" />



---

## 🛠️ Common Problems

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| **Outlook closes at startup** | A faulty add-in | Fix 1: Safe Mode |
| **Opens in Safe Mode only** | An add-in | Turn add-ins off, then on one at a time |
| **`Cannot start Microsoft Outlook`** | A damaged profile, or a corrupted navigation pane | Fix 3: a new profile |
| **`The set of folders cannot be opened`** | A damaged data file or profile | Fix 2, then Fix 3 |
| **Mail does not load, but webmail works** | A damaged OST or profile | Fix 2, then Fix 3 |
| **Sign-in prompts keep returning** | An authentication problem | See [Outlook Sign-in and Profile Troubleshooting](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/outlook-sign-in-and-profile-problems.md) |




---

## 💡 Next Step

→ [Outlook Sign-in and Profile Troubleshooting](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Outlook%20and%20Exchange%20Online/outlook-sign-in-and-profile-problems.md)






















