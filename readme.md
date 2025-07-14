# GNOME Arch Setup

This repository stores my GNOME Shell configuration for Arch Linux.  
The main file is:

- `gnome_extension_settings_01.txt`:  
  Output from `dconf dump /org/gnome/shell/extensions/`  
  This can be restored on another system using `dconf load`.

---

## 🧩 Extensions Used

Here are the GNOME Shell extensions included in my configuration:

- ArcMenu
- Astra Monitor
- Auto Move Windows
- Blur My Shell
- Burn My Windows
- Caffeine
- Clipboard History
- Compact Top Bar
- Custom Hot Corners Extended
- Dash to Dock
- Dash to Panel
- Ding
- Extension List
- Hide Top Bar
- Just Perfection
- Move Clock
- Space Bar
- Status Area Horizontal Spacing
- System Monitor
- User Themes
- Vitals
- Weather O'Clock

---

## 🔧 How to Install GNOME Shell Integration (Host + Browser)

### On Arch Linux:

Install the native host connector:

```bash
sudo pacman -S gnome-browser-connector
```

This installs the native messaging host that allows the browser extension to communicate with GNOME Shell.

---

## 🌐 Browser Extension Required

To manage extensions from the browser, you must install this browser extension:

➡️ **[GNOME Shell Integration Extension](https://extensions.gnome.org/)**
(Available for Firefox and Chromium-based browsers)

Once installed, you can manage your GNOME extensions at:
🔗 [https://extensions.gnome.org/local/](https://extensions.gnome.org/local/)

---

## 📥 Restoring Extension Settings

To restore the GNOME extension settings from this repo:

```bash
dconf load /org/gnome/shell/extensions/ < gnome_extension_settings_01.txt
```

---

## 🗂️ Notes

The dconf file (the .txt file) has many more extension settings, that I actually dont use. It's because removing a GNOME extension doesn't automatically clean up its dconf settings.But it's not a problem because dconf load is safe and doesn't break anything if some extensions listed in the input aren’t installed.
