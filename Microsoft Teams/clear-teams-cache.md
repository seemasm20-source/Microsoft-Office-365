
# Microsoft Teams Cache Clearing Troubleshooting


## Objective

Troubleshoot Microsoft Teams performance and display issues that may be caused by corrupted or outdated local cache data.

## Symptoms of Cache Issues

- Teams loads very slowly.
- Teams freezes or becomes unresponsive.
- Old messages or files appear temporarily.
- Profile picture does not update.
- Presence or availability status does not update correctly.

*Note: These symptoms can have other causes, so clearing the cache is not guaranteed to resolve them.*

## 1. Completely Close Microsoft Teams

**Method A - Quit Teams**

1. Right-click the Teams icon in the system tray near the clock.
2. Select **Quit**.

**Method B - Use Task Manager**

1. Press **Ctrl + Shift + Esc** to open Task Manager.
2. Find **Microsoft Teams** in the Processes list.
3. Select Teams → click **End task**.
4. Confirm that Teams is no longer running.

Use Task Manager if Teams is frozen or does not close normally.

## 2. Clear the Teams Cache

### For Classic Teams

1. Press **Win + R** to open the Run dialog.
2. Enter the following path:

   `%appdata%\Microsoft\Teams`

3. Press Enter.
4. If the folder exists, delete its cache contents or the relevant cache folders, such as:
   - `Cache`
   - `blob_storage`
   - `databases`
   - `GPUCache`
   - `IndexedDB`
   - `Local Storage`
   - `tmp`

5. If a folder does not exist, skip it. Do not delete unrelated files.




## 4. Verification Checklist

- [ ] Teams starts without freezing.
- [ ] Loading performance has improved.
- [ ] Messages and files display correctly.
- [ ] Profile picture and presence status update.
- [ ] The result is recorded in the support ticket.



<img width="1920" height="1080" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/a4bedbeb-3095-4dc4-af8e-0fc1204ad917" />











<img width="1920" height="1080" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/10246c91-c93f-4963-90d6-9e025560600b" />







<img width="1920" height="1080" alt="Screenshot (77)" src="https://github.com/user-attachments/assets/f476cc8b-34b8-42d0-bd7c-537ed6049e38" />










<img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/384105b6-b333-4917-aefc-37fe5eb97a5a" />
