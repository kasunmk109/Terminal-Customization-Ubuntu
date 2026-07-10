<div align="center">

# ⚡ Ubuntu Cyber Terminal Setup
### Transform your Ubuntu terminal into a modern developer workspace

Custom anime artwork • ZSH • Fastfetch • Kitty • Nerd Fonts • Ubuntu 24.04

!Ubuntu
!Shell
!Terminal
!Fastfetch

</div>

---

# ✨ Features

This setup gives you:

✅ Clean cyberpunk terminal UI
✅ Custom anime image support
✅ Beautiful developer fonts
✅ Fast system information with Fastfetch
✅ ZSH shell customization
✅ Kitty GPU accelerated terminal
✅ Easy restore to original terminal
✅ Beginner friendly installation guide

---

# 🖼 Preview

<img src="./Screenshot from 2026-05-03 11-42-27.png" width="100%">

---

# 📦 Repository Structure

```bash
.
├── assets/
│ └── jedi.png
├── config.jsonc
├── Screenshot from 2026-05-03 11-42-27.png
├── LICENSE
└── README.md
```

---

# 🖥 Tested Environment

| Component | Version |
|---|---|
| Ubuntu | 24.04.4 LTS |
| Desktop | GNOME 46 |
| Shell | ZSH |
| Terminal | Kitty |
| System Info | Fastfetch |

---

# 🚀 Installation Guide

---

# 1️⃣ Update Ubuntu

Always start with an updated system.

```bash
sudo apt update && sudo apt upgrade -y
```

---

# 2️⃣ Download Developer Fonts

Visit:

https://fonts.google.com/

Recommended:

## JetBrains Mono

Download the font zip file.

---

## Extract font

Example:

```bash
cd ~/Downloads
unzip JetBrains_Mono.zip
```

---

## Install font

Create fonts directory:

```bash
mkdir -p ~/.fonts
```

Copy fonts:

```bash
cp -r JetBrainsMono-* ~/.fonts/
```

Refresh font cache:

```bash
fc-cache -fv
```

Verify:

```bash
fc-list | grep "JetBrains"
```

---

# 3️⃣ Install ZSH Shell

Install:

```bash
sudo apt install zsh -y
```

Verify:

```bash
zsh --version
```

Set ZSH as default shell:

```bash
chsh -s $(which zsh)
```

Logout and login again.

Verify:

```bash
echo $SHELL
```

Expected:

```bash
/usr/bin/zsh
```

---

# 4️⃣ Backup Original Terminal Profile

Before customization, create a backup profile.

Open GNOME Terminal.

Go to:

```text
Preferences → Profiles
```

Duplicate current profile.

Rename it:

```text
Default Backup
```

Now you can always restore original settings.

---

# 5️⃣ Install Fastfetch

Download and install latest Fastfetch.

```bash
wget -qO fastfetch.tar.gz https://github.com/fastfetch-cli/fastfetch/releases/latest/download/fastfetch-linux-amd64.tar.gz
```

Install:

```bash
sudo tar xf fastfetch.tar.gz --strip-components=3 -C /usr/local/bin fastfetch-linux-amd64/usr/bin/fastfetch
```

Remove archive:

```bash
rm fastfetch.tar.gz
```

Verify:

```bash
fastfetch
```

---

# 6️⃣ Generate Fastfetch Config

Generate config file:

```bash
fastfetch --gen-config
```

This creates:

```bash
~/.config/fastfetch/config.jsonc
```

---

# 7️⃣ Replace Fastfetch Config

Clone this repository:

```bash
git clone https://github.com/kasunmk109/Terminal-Customization-Ubuntu.git
cd Terminal-Customization-Ubuntu
```

Replace config:

```bash
cp config.jsonc ~/.config/fastfetch/
```

---

# 8️⃣ Add Image Assets

Create assets folder:

```bash
mkdir -p ~/.config/fastfetch/assets
```

Copy image:

```bash
cp assets/jedi.png ~/.config/fastfetch/assets/
```

---

# 9️⃣ Install Kitty Terminal

Kitty is required for PNG image rendering.

Install:

```bash
sudo apt install kitty -y
```

Verify:

```bash
kitty --version
```

Launch:

```bash
kitty
```

---

# 🔟 Set Kitty as Default Terminal

Run:

```bash
sudo update-alternatives --config x-terminal-emulator
```

Select:

```text
kitty
```

Optional GNOME setting:

```bash
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
```

Verify:

```bash
gsettings get org.gnome.desktop.default-applications.terminal exec
```

Expected:

```bash
'kitty'
```

---

# 1️⃣1️⃣ Auto Run Fastfetch

Open ZSH config:

```bash
nano ~/.zshrc
```

Add this at bottom:

```bash
command -v fastfetch >/dev/null && fastfetch
```

Save and apply:

```bash
source ~/.zshrc
```

---

# 1️⃣2️⃣ Test Setup

Open Kitty:

```bash
kitty
```

Your terminal should now display:

✅ Custom image
✅ System information
✅ Developer shell
✅ Modern cyber UI

---

# 🔄 Restore Original Terminal

If needed:

```bash
sudo update-alternatives --config x-terminal-emulator
```

Select:

```text
gnome-terminal
```

Or switch to your backup profile.

---
 
# 🎨 GNOME Extensions Manager - Desktop Customization
 
### What are GNOME Extensions?
 
GNOME Extensions are small programs that enhance your desktop experience. They can change icons, add themes, modify your taskbar, and much more. Perfect for beginners who want a personalized desktop without diving into complex configurations.
 
---
 
## 1️⃣ Install GNOME Extensions Manager
 
### Step 1: Open Terminal
 
```bash
kitty
```
 
### Step 2: Install Extensions Manager
 
```bash
sudo apt install gnome-shell-extension-manager -y
```
 
### Step 3: Verify Installation
 
```bash
extension-manager --version
```
 
---
 
## 2️⃣ Open Extensions Manager
 
### Method 1: Command Line
 
```bash
extension-manager
```
 
### Method 2: GUI
 
- Click "Show Applications" (grid icon bottom-left)
- Search for "Extensions Manager"
- Click to open
---
 
## 3️⃣ Recommended GNOME Extensions
 
### Essential Extensions for Beginners
 
| Extension | Purpose |
|---|---|
| **Dash to Panel** | Move dock to top panel like Windows taskbar |
| **Caffeine** | Prevent screen from locking |
| **Blur my Shell** | Add blur effect to background |
| **Just Perfection** | Fine-tune GNOME design |
| **AppIndicator and KStatusNotifierItem Support** | System tray icons |
| **Clipboard Indicator** | Clipboard history |
| **Tactile** | Organize windows by tiling |
 
---
 
## 4️⃣ Step-by-Step: Install Dash to Panel Extension
 
### Step 1: Open Extensions Manager
 
```bash
extension-manager
```
 
### Step 2: Search for Extension
 
- Click search icon (magnifying glass)
- Type: `Dash to Panel`
- Press Enter
### Step 3: Browse Results
 
Look for the official extension by author "jderose9"
 
### Step 4: Click Install
 
- Click the extension result
- Click blue **"Install"** button
- Wait for installation to complete
### Step 5: Enable Extension
 
- Toggle switch to **ON**
- You may see notification asking for confirmation
### Step 6: Verify
 
Look at top of screen - your dock should now appear as a panel at the top.
 
---
 
## 5️⃣ Customize Icon Themes
 
### Step 1: Install Icon Theme
 
Common icon theme options:
 
```bash
sudo apt install ubuntu-mono -y
sudo apt install gnome-icon-theme -y
sudo apt install papirus-icon-theme -y
sudo apt install tela-icon-theme -y
```
 
Choose one. Popular choice for cyberpunk look:
 
```bash
sudo apt install papirus-icon-theme -y
```
 
### Step 2: Apply Icon Theme
 
- Click "Show Applications" (grid icon)
- Search for **"Settings"**
- Open Settings
- Go to: **Appearance** → **Style** → **Icons**
- Select your installed theme (e.g., "Papirus")
- Close Settings - changes apply immediately
### Step 3: Verify Icons
 
Icons throughout your desktop should now match the new theme.
 
---
 
## 6️⃣ Customize Cursor Theme
 
### Step 1: Install Cursor Theme
 
```bash
sudo apt install breeze-cursor-theme -y
```
 
Or download from community:
 
```bash
git clone https://github.com/alacritty/alacritty.git ~/.local/share/cursors/Alacritty
```
 
### Step 2: Apply Cursor Theme
 
- Open **Settings**
- Go to: **Appearance** → **Style** → **Cursor**
- Select your cursor theme
- Apply
---
 
## 7️⃣ Customize GTK Theme (Application Look)
 
### Step 1: Install Theme
 
Popular modern themes:
 
```bash
# Adwaita Dark Theme (Default, sleek)
sudo apt install adwaita-icon-theme -y
 
# Or install Dracula (Cyberpunk style)
git clone https://github.com/dracula/gtk.git ~/.themes/Dracula
```
 
### Step 2: Apply Theme
 
- Open **Settings**
- Go to: **Appearance** → **Style** → **Application**
- Select your theme
- Restart applications to see changes
---
 
## 8️⃣ Install Blur My Shell Extension
 
### Step 1: Open Extensions Manager
 
```bash
extension-manager
```
 
### Step 2: Search and Install
 
- Search: `Blur my Shell`
- Click Install
- Toggle ON
### Step 3: Configure Blur
 
- In Extensions Manager, find "Blur my Shell"
- Click settings icon (gear)
- Adjust blur intensity and effects
- Changes apply instantly
---
 
## 9️⃣ Enable Just Perfection for Fine-Tuning
 
### Step 1: Install Extension
 
```bash
extension-manager
```
 
- Search: `Just Perfection`
- Install and enable
### Step 2: Open Preferences
 
- Right-click the extension
- Select **"Preferences"**
### Step 3: Customize
 
- **Visibility**: Show/hide elements
- **Blur**: Toggle blur effects
- **Panel**: Customize top panel
- **Activities Button**: Rename or hide
### Step 4: Apply
 
All changes apply in real-time.
 
---
 
## 🔟 Uninstall or Disable Extensions
 
### Disable (Keep Installed)
 
- Open Extensions Manager
- Toggle extension **OFF**
- Changes apply immediately
### Uninstall (Remove Completely)
 
- Open Extensions Manager
- Click on extension
- Click **"Remove"** button
- Confirm removal
---
 
---
 
# 🎚️ Conky - System Information Widgets
 
### What is Conky?
 
Conky is a system monitor that displays information like CPU usage, RAM, temperature, disk space, network speed, and more - as customizable widgets on your desktop. Perfect for developers who want real-time system monitoring.
 
---
 
## 1️⃣ Install Conky
 
### Step 1: Update System
 
```bash
sudo apt update
```
 
### Step 2: Install Conky
 
```bash
sudo apt install conky-all -y
```
 
### Step 3: Verify Installation
 
```bash
conky --version
```
 
Expected output:
 
```
Conky 1.x.x
```
 
---
 
## 2️⃣ Create Conky Configuration Directory
 
### Step 1: Create Directory
 
```bash
mkdir -p ~/.config/conky
```
 
### Step 2: List Contents
 
```bash
ls -la ~/.config/conky/
```
 
You should see an empty directory.
 
---
 
## 3️⃣ Create Your First Conky Config File
 
### Step 1: Create Config File
 
```bash
nano ~/.config/conky/conky.conf
```
 
### Step 2: Add Basic Configuration
 
Copy and paste this beginner-friendly config:
 
```lua
conky.config = {
    alignment = 'top_right',
    background = true,
    border_width = 1,
    cpu_avg_samples = 2,
    default_color = 'white',
    default_outline_color = 'white',
    default_shade_color = 'white',
    double_buffer = true,
    draw_borders = false,
    draw_graph_borders = true,
    draw_outline = false,
    draw_shades = false,
    extra_newline = false,
    font = 'DejaVu Sans Mono:size=10',
    gap_x = 10,
    gap_y = 10,
    line_height = 1,
    maximum_width = 300,
    net_avg_samples = 2,
    no_buffers = true,
    out_to_console = false,
    out_to_ncurses = false,
    out_to_stderr = false,
    out_to_x = true,
    own_window = true,
    own_window_class = 'Conky',
    own_window_type = 'desktop',
    own_window_transparent = true,
    pad_percents = 3,
    text_buffer_size = 256,
    update_interval = 1,
    uppercase = false,
    use_spacer = 'left',
    use_xft = true,
}
 
conky.text = [[
${color cyan}SYSTEM MONITOR${color}
${hr 2}
${color}Host:${color white} ${nodename}
${color}Kernel:${color white} ${kernel}
${color}Uptime:${color white} ${uptime}
 
${color cyan}CPU${color}
${hr 2}
${color}CPU 1:${color white} ${cpu cpu1}%
${color}CPU 2:${color white} ${cpu cpu2}%
${color}Average:${color white} ${cpu}%
${cpubar}
 
${color cyan}MEMORY${color}
${hr 2}
${color}RAM:${color white} ${mem} / ${memmax}
${membar}
${color}SWAP:${color white} ${swap} / ${swapmax}
 
${color cyan}DISK${color}
${hr 2}
${color}Root (${color white}/:${color}):${color white} ${fs_used /} / ${fs_size /}
${fs_bar /}
 
${color cyan}NETWORK${color}
${hr 2}
${color}Upload:${color white} ${upspeed wlan0}
${color}Download:${color white} ${downspeed wlan0}
 
${color cyan}TEMPERATURES${color}
${hr 2}
${color}CPU Temp:${color white} ${hwmon 0 temp 1}°C
]]
```
 
### Step 3: Save File
 
- Press **Ctrl + O**
- Press **Enter** to confirm
- Press **Ctrl + X** to exit
---
 
## 4️⃣ Test Conky Configuration
 
### Step 1: Run Conky
 
```bash
conky -c ~/.config/conky/conky.conf
```
 
### Step 2: Verify Display
 
- Look at top-right corner of desktop
- You should see system information widget
- Check if all values are displaying correctly
### Step 3: Stop Conky
 
- Press **Ctrl + C** in terminal
---
 
## 5️⃣ Advanced: Create Cyberpunk-Styled Conky
 
### Step 1: Create New Config File
 
```bash
nano ~/.config/conky/conky_cyberpunk.conf
```
 
### Step 2: Add Cyberpunk Theme
 
```lua
conky.config = {
    alignment = 'bottom_right',
    background = true,
    border_width = 2,
    cpu_avg_samples = 2,
    default_color = '#00FF00',
    default_outline_color = '#00AA00',
    default_shade_color = '#000000',
    double_buffer = true,
    draw_borders = true,
    draw_graph_borders = true,
    draw_outline = true,
    draw_shades = true,
    extra_newline = false,
    font = 'JetBrains Mono:size=9',
    gap_x = 15,
    gap_y = 15,
    line_height = 1,
    maximum_width = 320,
    net_avg_samples = 2,
    no_buffers = true,
    out_to_x = true,
    own_window = true,
    own_window_class = 'Conky',
    own_window_type = 'desktop',
    own_window_transparent = true,
    own_window_argb_visual = true,
    own_window_argb_value = 240,
    pad_percents = 3,
    text_buffer_size = 256,
    update_interval = 1,
    uppercase = false,
    use_spacer = 'left',
    use_xft = true,
}
 
conky.text = [[
${color #00FF00}╔═══════════════════════════╗${color}
${color #00FF00}║${color}   CYBER SYSTEM MONITOR   ${color #00FF00}║${color}
${color #00FF00}╚═══════════════════════════╝${color}
 
${color #00FF00}▸${color} ${nodename}
${color #00FF00}▸${color} ${kernel}
${color #00FF00}▸${color} Uptime: ${uptime}
 
${color #FF00FF}[CPU STATUS]${color}
${color #00FF00}├─${color} Core 1: ${cpu cpu1}%
${color #00FF00}├─${color} Core 2: ${cpu cpu2}%
${color #00FF00}└─${color} Avg: ${cpu}%
${color #00AA00}${cpubar}${color}
 
${color #FF00FF}[MEMORY STATUS]${color}
${color #00FF00}├─${color} RAM: ${mem}/${memmax}
${color #00AA00}${membar}${color}
${color #00FF00}└─${color} SWAP: ${swap}/${swapmax}
 
${color #FF00FF}[DISK STATUS]${color}
${color #00FF00}└─${color} /: ${fs_used /}/${fs_size /}
${color #00AA00}${fs_bar /}${color}
 
${color #FF00FF}[NETWORK]${color}
${color #00FF00}├─${color} ↑ ${upspeed wlan0}
${color #00FF00}└─${color} ↓ ${downspeed wlan0}
 
${color #FF00FF}[TEMPERATURE]${color}
${color #00FF00}└─${color} CPU: ${hwmon 0 temp 1}°C
]]
```
 
### Step 3: Save and Test
 
```bash
conky -c ~/.config/conky/conky_cyberpunk.conf
```
 
---
 
## 6️⃣ Auto-Start Conky on Boot
 
### Step 1: Create Startup Script
 
```bash
mkdir -p ~/.config/autostart
nano ~/.config/autostart/conky.desktop
```
 
### Step 2: Add Script Content
 
```ini
[Desktop Entry]
Type=Application
Name=Conky
Comment=System Monitoring Widget
Exec=conky -c ~/.config/conky/conky_cyberpunk.conf
StartupNotify=false
Hidden=false
Terminal=false
Categories=System;Utility;
```
 
### Step 3: Save
 
- Press **Ctrl + O**
- Press **Enter**
- Press **Ctrl + X**
### Step 4: Make Executable
 
```bash
chmod +x ~/.config/autostart/conky.desktop
```
 
### Step 5: Restart Desktop
 
- Log out
- Log back in
Conky should now appear automatically when you login.
 
---
 
## 7️⃣ Conky Configuration Variables (Common)
 
### CPU & System
 
```lua
${cpu}                 -- Average CPU usage percentage
${cpu cpu1}            -- CPU core 1 usage
${cpu cpu2}            -- CPU core 2 usage
${cpubar}              -- CPU usage bar graph
${kernel}              -- Kernel version
${uptime}              -- System uptime
${nodename}            -- Computer name
```
 
### Memory
 
```lua
${mem}                 -- RAM used
${memmax}              -- Total RAM
${membar}              -- RAM usage bar
${swap}                -- Swap used
${swapmax}             -- Total swap
```
 
### Disk
 
```lua
${fs_used /}           -- Disk used (/)
${fs_size /}           -- Total disk size (/)
${fs_bar /}            -- Disk usage bar
${fs_free /}           -- Disk free space
```
 
### Network
 
```lua
${downspeed wlan0}     -- Download speed
${upspeed wlan0}       -- Upload speed
${addr wlan0}          -- IP address
${totaldown wlan0}     -- Total download
${totalup wlan0}       -- Total upload
```
 
### Temperature
 
```lua
${hwmon 0 temp 1}      -- CPU temperature core 1
${hwmon 0 temp 2}      -- CPU temperature core 2
${acpitemp}            -- System temperature
```
 
### Date & Time
 
```lua
${time %H:%M:%S}       -- Current time (HH:MM:SS)
${time %d/%m/%Y}       -- Current date
${time %A}             -- Day of week
```
 
---
 
## 8️⃣ Advanced: Multiple Conky Windows
 
### Step 1: Create Second Config
 
```bash
nano ~/.config/conky/conky_sidebar.conf
```
 
### Step 2: Add Different Position
 
```lua
conky.config = {
    alignment = 'top_left',
    -- ... rest of config ...
}
 
conky.text = [[
${color cyan}QUICK INFO${color}
${hr 2}
Time: ${time %H:%M:%S}
Date: ${time %d/%m/%Y}
]]
```
 
### Step 3: Create Launcher Script
 
```bash
nano ~/.config/conky/start_conky.sh
```
 
### Step 4: Add Script Content
 
```bash
#!/bin/bash
conky -c ~/.config/conky/conky_cyberpunk.conf &
conky -c ~/.config/conky/conky_sidebar.conf &
```
 
### Step 5: Make Executable
 
```bash
chmod +x ~/.config/conky/start_conky.sh
```
 
### Step 6: Test
 
```bash
~/.config/conky/start_conky.sh
```
 
---
 
## 9️⃣ Troubleshooting Conky
 
### Issue: Conky won't start
 
**Solution:**
 
```bash
# Check if there's a running instance
ps aux | grep conky
 
# Kill existing process
killall conky
 
# Try starting again
conky -c ~/.config/conky/conky.conf
```
 
### Issue: Values show as N/A
 
**Solution:**
 
```bash
# Check available hardware info
sensors
 
# If needed, install lm-sensors
sudo apt install lm-sensors -y
sudo sensors-detect
```
 
### Issue: Text appears blurry
 
**Solution:**
 
Change font size in config:
 
```lua
font = 'JetBrains Mono:size=10',  -- Increase size
```
 
### Issue: High CPU usage
 
**Solution:**
 
Increase update interval:
 
```lua
update_interval = 2,  -- Update every 2 seconds instead of 1
```
 
---
 
## 🔟 Stop or Remove Conky
 
### Stop Conky Temporarily
 
```bash
killall conky
```
 
### Remove Auto-Start
 
```bash
rm ~/.config/autostart/conky.desktop
```
 
### Remove Configuration
 
```bash
rm -rf ~/.config/conky
```
 
---
 
---
 
# 🔄 Restore Original Terminal
 
If needed:
 
```bash
sudo update-alternatives --config x-terminal-emulator
```
 
Select:
 
```text
gnome-terminal
```
 
Or switch to your backup profile.
 
---
 
# 📁 Included Files
 
## Fastfetch Config
 
```bash
config.jsonc
```
 
## Custom Artwork
 
```bash
assets/jedi.png
```
 
## Screenshot
 
```bash
Screenshot from 2026-05-03 11-42-27.png
```
 
---
 
# 🎯 Quick Reference - All Commands
 
### Terminal & Shell
 
```bash
zsh --version
chsh -s $(which zsh)
fastfetch
source ~/.zshrc
```
 
### Extensions Manager
 
```bash
extension-manager
sudo apt install gnome-shell-extension-manager -y
```
 
### Icon & Theme Themes
 
```bash
sudo apt install papirus-icon-theme -y
sudo apt install breeze-cursor-theme -y
```
 
### Conky
 
```bash
sudo apt install conky-all -y
conky -c ~/.config/conky/conky.conf
killall conky
```
 
### Kitty Terminal
 
```bash
kitty
kitty --version
sudo update-alternatives --config x-terminal-emulator
```
 
---
 
# 📞 Support & Troubleshooting
 
### Common Issues
 
**Terminal looks weird after update:**
```bash
source ~/.zshrc
```
 
**Extensions not working:**
- Restart GNOME Shell: Press Alt + F2, type `r`, press Enter
**Conky not showing:**
```bash
killall conky
conky -c ~/.config/conky/conky_cyberpunk.conf
```
 
**Font not applying:**
```bash
fc-cache -fv
```
 
---
 
# 👨‍💻 Author
 
# Kasun Mahela
 
Electrical and Computer Engineering Undergraduate  
The Open University of Sri Lanka  
 
---
 
# 📬 Contact Me
 
If you face any issues while setting up this project, feel free to contact me.
 
📱 WhatsApp: +94 71 215 1023  
📧 Email: kasunmahela2020.am@gmail.com  
 
---
 
# 📜 License
 
This project is licensed under the Apache License 2.0.  
 
See the `LICENSE` file for more details.
 
---
 
<div align="center">
### ⭐ If this repository helped you, please consider starring the repo.
 
</div>
