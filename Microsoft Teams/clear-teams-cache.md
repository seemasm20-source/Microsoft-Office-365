# ☁️ Microsoft Teams - Cache Clearing Troubleshooting

[ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---




## 📋 Summary

Troubleshoot Microsoft Teams performance and display problems that may come from corrupted or outdated local cache data, by fully closing Teams, clearing its cache folder and starting it again. Teams problems are a frequent ticket for an IT Help Desk Tier 1 and Tier 2 technician.



---



## 💡 What is the Teams Cache?

Teams stores temporary data on the computer, such as messages, images, files and settings, so it loads faster. If this data becomes corrupted or outdated, Teams can behave badly. Clearing the cache removes the local copy, and Teams downloads fresh data from the server the next time it starts. No messages or files are lost, because they are stored in Microsoft 365, not in the cache.

| Setting | Value |
|---------|-------|
| **Client** | New Microsoft Teams (Windows 10 and 11) |
| **Cache folder** | `%localappdata%\Packages\MSTeams_8wekyb3d8bbwe\LocalCache\Microsoft\MSTeams` |
| **Process name** | `ms-teams.exe` (shown as **Microsoft Teams** in Task Manager) |

### Symptoms of a Cache Problem

- Teams loads very slowly
- Teams freezes or does not respond
- Old messages or files appear for a while
- The profile picture does not update
- The presence or availability status does not update correctly

> These symptoms can have other causes, such as a poor connection or a Microsoft 365 service problem, so clearing the cache does not always fix them. Check the network and the service status as well.

---

## 🔧 Steps

### Step 1 - Close Teams Completely

**Method A - Quit Teams**

1. Right-click the Teams icon in the system tray, near the clock.
2. Select **Quit**.

**Method B - Task Manager** (if Teams is frozen or does not close)

1. Press **Ctrl + Shift + Esc** to open Task Manager.
2. Find **Microsoft Teams** in the **Processes** list.
3. Select it and click **End task**.
4. Check that no Teams process is still running.

**Screenshot: Teams closed:**

<img width="1920" height="1080" alt="Task Manager with the Microsoft Teams process ended" src="https://github.com/user-attachments/assets/a4bedbeb-3095-4dc4-af8e-0fc1204ad917" />







<img width="1920" height="1080" alt="Run dialog with the Teams cache path entered" src="https://github.com/user-attachments/assets/10246c91-c93f-4963-90d6-9e025560600b" />




### Step 2 - Clear the Cache

1. Press **Win + R** to open the **Run** dialog.
2. Enter the cache folder path and press **Enter**:

```text
%localappdata%\Packages\MSTeams_8wekyb3d8bbwe\LocalCache\Microsoft\MSTeams
```

3. File Explorer opens the folder. Select **all files and folders inside it** (**Ctrl + A**) and delete them.
4. If Windows says a file is in use, close Teams again and retry, or skip that file.

> Delete only the contents of the `MSTeams` folder. Do not delete the whole `MSTeams_8wekyb3d8bbwe` folder, which holds other app data and settings.

**Screenshots: cache folder:**



<img width="1920" height="1080" alt="The MSTeams cache folder with its contents selected for deletion" src="https://github.com/user-attachments/assets/f476cc8b-34b8-42d0-bd7c-537ed6049e38" />




### Step 3 - Restart Teams

1. Open Teams from the Start menu and sign in if asked.
2. The first start takes longer than usual, because Teams rebuilds its cache.

**Screenshot: Teams restarted:**

<img width="1920" height="1080" alt="Microsoft Teams started again after clearing the cache" src="https://github.com/user-attachments/assets/384105b6-b333-4917-aefc-37fe5eb97a5a" />

---

## ✅ Verification

- [ ] Teams starts without freezing
- [ ] Loading is faster
- [ ] Messages and files display correctly
- [ ] The profile picture and the presence status update
- [ ] The result is recorded in the support ticket

---

## 🛠️ If the Problem Continues

| Next step | How |
|-----------|-----|
| **Repair or reset the app** | **Settings → Apps → Installed apps → Microsoft Teams → ⋯ → Advanced options → Repair**. If it still fails, choose **Reset**. Reset removes the app's local data, so the user signs in again |
| **Update Teams** | Open Teams, select the three dots, then **Settings → About Teams**, and check for updates |
| **Try Teams in a browser** | Sign in at `teams.microsoft.com`. If the web version works, the problem is in the desktop app |
| **Check the network** | `ping 8.8.8.8` and `nslookup teams.microsoft.com` |
| **Check the service status** | Microsoft 365 Admin Center → **Health → Service health** |

---

## 📝 Classic Teams (Retired)

Classic Teams stored its cache in `%appdata%\Microsoft\Teams`, and clearing that folder does not clear the cache of the new Teams. Classic Teams has been retired and no longer runs, so these steps apply only to old installations.

---

## 💡 Next Step

→ [Run Repair and Reset Teams](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Microsoft%20Teams/run-repair-reset-teams.md)


























