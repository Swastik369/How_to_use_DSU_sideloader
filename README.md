# Guide: Installing GSIs with DSU Sideloader

## What is DSU Sideloader?

DSU (Dynamic System Updates) lets you boot a GSI as a "test OS" without modifying, wiping, or risking your stock system or user data. DSU Sideloader is an open-source app that automates this for custom GSIs—you select, it installs and boots, and you can discard or revert any time.[1][7][4]


> **Prerequisites:**  
> - Android 10+ device with Dynamic Partitions  
> - Unlocked bootloader  
> - GSI image (e.g., from [Phh’s GSI List](https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list))  
> - DSU Sideloader app ([Download on GitHub Releases](https://github.com/VegaBobo/DSU-Sideloader/releases))  

---

## 1. Install DSU Sideloader

1. Download the DSU Sideloader `.apk` from the [official GitHub releases](https://github.com/VegaBobo/DSU-Sideloader/releases).
2. Install the app and open it.
3. On first launch, give permission to a folder (create a new folder as prompted for DSU Sideloader's temp files).



## 2. Prepare Your GSI

- Download your preferred GSI (must match your device architecture and partition type: `arm/arm64`, `a/b`, etc.).
- Supported formats for the app: `.img`, `.gz`, `.xz`, `.zip` (DSU packages only).
- Place the GSI in accessible storage (e.g., Downloads).



## 3. Use DSU Sideloader to Install GSI

1. **Open DSU Sideloader.**
2. Tap on the button to **select GSI**; browse and pick your GSI file.
3. (Optional) Adjust userdata size if needed—leave system size as default unless you know what you’re doing.
4. Tap **Install**.
5. Wait—installation may take a few minutes.

- After install, you may see a prompt:
   - On rooted or Shizuku-enabled devices, a DSU confirmation screen will appear directly on your phone.  
   - On non-rooted devices, you’ll see ADB instructions (run a provided command in your PC’s terminal).



## 4. Boot and Use Dynamic System

- Once the process is done, a persistent notification will appear to boot into the GSI ("Dynamic System").
- Tap **Restart** in the notification or, if provided, use the app to reboot.
- Your phone will boot into the GSI—your main system is untouched.
- To return to your stock system: **just reboot again**.


## 5. Remove/Discard GSI

- Find the same DSU notification and tap **Discard** to remove the GSI and revert unused space.
- Or, simply reboot into stock OS; the GSI remains available until you discard or factory reset.



## Tips & Troubleshooting

- **If stuck or bootloops:** Just reboot—the original system will come back.
- **Correct arch/slot:** Always match GSI’s architecture and partition type to your phone (check with Treble Info app).
- **Sticky mode:** On some devices, GSI can stay across reboots; see developer docs for toggle commands if needed.
- **You do NOT need root for basic DSU Sideloader usage, but Shizuku/root modes add more features and fewer manual steps.**

## Special Thanks to dev of DSU sideloader application 

