<div align="center">

# ⚡ Ubuntu Cyber Terminal Setup
### Transform your Ubuntu terminal into a modern developer workspace

Custom anime artwork • ZSH • Fastfetch • Kitty • Nerd Fonts • Ubuntu 24.04

![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04.4_LTS-E95420?style=for-the-badge&logo=ubuntu)
![Shell](https://img.shields.io/badge/Shell-ZSH-89e051?style=for-the-badge)
![Terminal](https://img.shields.io/badge/Terminal-Kitty-blue?style=for-the-badge)
![Fastfetch](https://img.shields.io/badge/System-Fastfetch-black?style=for-the-badge)

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
│   └── jedi.png
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
