

# ☁️ Microsoft Teams - Microphone, Camera and Meeting Troubleshooting

 [ Back to README] → [README](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/README.md)

---

## 📋 Summary

Troubleshoot microphone, speaker and camera problems in Microsoft Teams meetings, by checking the Teams device settings, the Windows privacy permissions and the physical device. Audio and video problems in meetings are among the most common tickets for an IT Help Desk Tier 1 and Tier 2 technician.

---

## 💡 Where Can the Problem Be?

A microphone or camera problem can come from four places, so work through them in order, from the simplest to the hardest.

| Layer | Examples |
|-------|----------|
| **Teams settings** | The wrong microphone, speaker or camera is selected |
| **Windows settings** | Privacy permissions are off, or the wrong sound device is the default |
| **The device** | Unplugged, muted by a hardware switch, in use by another app, or a driver problem |
| **The meeting** | The organiser or an administrator restricts the microphone or camera |

> **First question:** does the device fail only in Teams, or in other apps too? Failing everywhere points to Windows or the device. Failing only in Teams points to Teams settings or the meeting.

---

## 🔧 Part 1 - Diagnose Audio and Video Issues

### Step 1 - Check the Teams Device Settings

1. Open Teams, select **Settings and more (⋯) → Settings → Devices**.
2. Check that the correct **microphone**, **speaker** and **camera** are selected.

> Menu names can differ between Teams versions.

### Step 2 - Make a Test Call

On the same **Devices** page, select **Make a test call**, if it is available. Check that the microphone, speakers and camera work.

**Screenshot: Teams device settings:**

<img width="1920" height="1080" alt="Teams Settings Devices page with the microphone, speaker and camera selected" src="https://github.com/user-attachments/assets/6418bf62-1046-46ea-ac9d-9fb7d2337d6a" />

### Step 3 - Check the Microphone Permission in Windows

1. Open **Settings → Privacy & security → Microphone**.
2. Turn on **Microphone access** and **Let apps access your microphone**.
3. Turn on **Let desktop apps access your microphone**.
4. In the app list, check that **Microsoft Teams** is allowed, if it is listed.


### Step 4 - Check Device Manager

1. Right-click **Start** and select **Device Manager**.
2. Expand **Audio inputs and outputs**, **Sound, video and game controllers** and **Cameras**.
3. Look for a warning icon (a yellow triangle) or a disabled device.

**Screenshots: Windows privacy settings:**

<img width="1920" height="1080" alt="Windows Settings Privacy and security Microphone with access turned on" src="https://github.com/user-attachments/assets/89a486a1-30ba-466a-bd4e-d02d41115d88" />

<img width="1920" height="1080" alt="Windows Settings Privacy and security Camera with access turned on" src="https://github.com/user-attachments/assets/333b5a75-ae71-4ab7-b397-3b2a0ca175a2" />

### Step 5 - Check the Windows Sound Settings

Open **Settings → System → Sound**. Check that the correct **output** and **input** devices are selected, the volume is not zero, and the device is not muted.

### Step 6 - Check the Physical Device

- The headset or camera is connected, and the cable is not damaged
- No hardware mute switch or camera shutter is on
- No other application, such as another meeting app or a browser tab, is using the device
- A Bluetooth headset is connected and charged, and it is the selected device


---

## 🔧 Part 2 - Microphone or Camera Not Working Only in Meetings

1. Join the meeting and check the microphone and camera buttons in the meeting toolbar. A crossed-out icon means the device is off.
2. Check the device settings inside the meeting (the **⋯ More → Settings → Device settings** menu), and select the correct microphone and camera.
3. Check whether the meeting restricts the microphone or camera. The meeting options of the organiser, such as **Allow mic for attendees** and **Allow camera for attendees**, and the administrator's meeting policies, can switch them off for some participants. Ask the organiser to review the meeting options. An organiser cannot always unmute another participant directly.
4. Leave the meeting and join again.
5. If the problem continues, test the device in the Teams settings or another permitted application. This shows whether the problem is only in Teams.

---

## 🔧 Part 3 - Microphone or Camera Not Detected

1. Disconnect the headset or camera and connect it again, or use another USB port.
2. Close applications that may be using the device.
3. Restart Teams and test again.
4. In Device Manager, check whether the device is disabled or shows a driver warning.
5. If a driver update is needed, follow your organisation's approved driver update process.
6. If Teams still does not show the device, clear the Teams cache. See [Teams Cache Clearing Troubleshooting](./teams-cache-clearing.md).

> **Caution:** Do not uninstall drivers or change device settings without following your organisation's support procedure.

---

## 🛠️ Common Problems

| Symptom | Likely cause | What to check |
|---------|--------------|---------------|
| **Others cannot hear the user** | The wrong microphone is selected, or the microphone is muted | Teams device settings, the mute button, Windows Sound input |
| **The user cannot hear others** | The wrong speaker is selected, or the volume is low | Teams device settings, Windows Sound output and volume |
| **The camera shows a black screen or "camera in use"** | Another app is using the camera, or the privacy setting is off | Close other apps, check the camera permission |
| **The device is missing from the Teams list** | The device is not detected, or Windows blocks it | Device Manager, the privacy settings, another USB port |
| **The microphone works in other apps but not in Teams** | A Teams setting or permission | Teams device settings, **Let desktop apps access your microphone**, and the Teams cache |
| **The microphone is blocked in meetings only** | Meeting options or an administrator policy | The organiser's meeting options, and the Teams meeting policy in the admin settings |
| **The Bluetooth headset sounds poor or has no microphone** | The headset is using the wrong profile | Select the headset as both the input and the output in Teams |

---

## ✅ Verification

- [ ] The correct microphone, speaker and camera are selected
- [ ] The microphone and speaker pass the test call
- [ ] The camera preview works
- [ ] The user can hear and be heard in a test meeting
- [ ] The issue is resolved, or the steps taken are documented in the ticket

---

## 💡 Next Step

→ [Microphone, Camera and Meetings](https://github.com/seemasm20-source/Microsoft-Office-365/blob/main/Microsoft%20Teams/microphone-camera-and-meetings.md)



