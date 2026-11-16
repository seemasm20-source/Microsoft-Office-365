# ☁️ Microsoft Teams - Repair, Reset and Reinstall

[ Back to Overview] → [README.md](./README.md)

---

## 📋 Summary

Fix Microsoft Teams desktop app problems, such as crashes, freezing, failure to open, or problems that continue after basic troubleshooting, by using Repair, Reset and, as the last step, Reinstall. The steps go from the least to the most disruptive, so the user loses as little as possible.

---

## 💡 Which Fix First?

| Order | Fix | What it does | What the user loses |
|:-----:|-----|--------------|---------------------|
| 1 | **Clear the cache** | Deletes temporary data | Nothing. Teams starts more slowly the first time |
| 2 | **Repair** | Tries to fix the app without deleting its data | Nothing |
| 3 | **Reset** | Reinstalls the app's data to its default state | Local app data, saved settings and the sign-in state. The user signs in again |
| 4 | **Reinstall** | Removes the app and installs it again | Same as Reset, and the app is installed again |

> Messages, files and meetings are stored in Microsoft 365, not on the computer, so none of these fixes deletes them. Start with [Teams Cache Clearing](./teams-cache-clearing.md) if you have not already.

| Setting | Value |
|---------|-------|
| **Client** | New Microsoft Teams (Windows 10 and 11) |
| **Tool** | Windows **Settings → Apps → Installed apps** |
| **Official download** | [microsoft.com/microsoft-teams/download-app](https://www.microsoft.com/en-us/microsoft-teams/download-app) |

---

## 🔧 Part 1 - Repair Microsoft Teams

1. Open **Windows Settings → Apps → Installed apps**.
2. Search for **Microsoft Teams**.
3. Click the **three-dot menu (⋯)** next to Teams and select **Advanced options**.
4. Under **Reset**, click **Repair** and wait for it to finish.
5. Open Teams again and test the function that failed.

**Screenshot: Advanced options with Repair and Reset:**

<img width="1920" height="1080" alt="Windows Settings Advanced options page for Microsoft Teams with the Repair and Reset buttons" src="https://github.com/user-attachments/assets/106ad893-8f49-4eb0-b3ae-2e10f95753c4" />

> **Note:** Repair tries to fix the app without deleting its data.

---

## 🔧 Part 2 - Reset Microsoft Teams

Use Reset if Repair does not fix the problem.

1. Open **Settings → Apps → Installed apps**, search for **Microsoft Teams**, click **⋯** and select **Advanced options**.
2. Click **Reset** and confirm.
3. Open Teams and sign in again.
4. Test whether the original problem is fixed.

**Screenshot: Reset confirmation:**

<img width="1920" height="1080" alt="Reset confirmation window for Microsoft Teams" src="https://github.com/user-attachments/assets/53a5fde3-3814-4521-80db-f1910d2d53ce" />

> **Caution:** Reset deletes the app's local data, including saved settings and the sign-in state. Tell the user before you start, so they have their sign-in details ready.

---

## 🔧 Part 3 - Reinstall Microsoft Teams

Use Reinstall if Repair and Reset do not fix the problem.

1. Open **Settings → Apps → Installed apps**.
2. Find **Microsoft Teams**, click **⋯** and select **Uninstall**.
3. Follow the prompts until the uninstall finishes.
4. Download Teams from the official Microsoft website: <https://www.microsoft.com/en-us/microsoft-teams/download-app>
5. Install Teams and sign in with the user's work or school account.
6. Test the function that failed.

> **Managed devices:** On company computers, Teams may be installed and updated by IT with a management tool such as Intune. Follow your organisation's software installation policy. If the reinstall is blocked, or Teams comes back in the same broken state, ask your administrator.

---

## ✅ Verification

- [ ] Teams opens without crashing or freezing
- [ ] The user can sign in
- [ ] Chats and teams load correctly
- [ ] The original problem no longer occurs
- [ ] The result is documented in the support ticket

---

## 🛠️ If the Problem Continues

| Check | How |
|-------|-----|
| **Windows updates** | **Settings → Windows Update**, install pending updates and restart |
| **Teams in a browser** | Sign in at `teams.microsoft.com`. If the web version works, the problem is in the desktop app |
| **Network and service status** | `ping 8.8.8.8`, and Microsoft 365 Admin Center → **Health → Service health** |
| **A different Windows profile** | Sign in with another Windows account. If Teams works there, the problem is in the user's profile |
| **Escalate** | Record what you tried and the exact error, and pass it to the next support level |

---

## 💡 Next Step

→ [Teams Troubleshooting Overview](./teams-overview.md)


























