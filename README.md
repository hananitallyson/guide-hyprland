# GUIDE-HYPRLAND

```bash
sudo pacman -S --needed base-devel git
git clone https://aur.archlinux.org/paru.git /tmp/paru
cd /tmp/paru
makepkg -si

```

```bash
# Official Repositories
sudo pacman -S --needed \
    hyprland waybar swww dunst thunar pamixer pavucontrol \
    wl-clipboard cliphist grim slurp fastfetch \
    fish vim neovim tree-sitter-cli nwg-look \
    tar zip unzip xdg-user-dirs ttf-ubuntu-mono-nerd

# AUR Packages
paru -S --needed tofi xcursor-pro-cursor-theme

```

```bash
# Set Fish as default shell
echo $(which fish) | sudo tee -a /etc/shells
chsh -s $(which fish)

# Initialize standard XDG user directories
xdg-user-dirs-update

```
