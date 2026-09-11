# GUIDE-HYPRLAND

```bash
# Set up base tools & paru
sudo pacman -S --needed base-devel git
git clone https://aur.archlinux.org/paru.git /tmp/paru
cd /tmp/paru
makepkg -si

```

```bash
# Install system packages
sudo pacman -S --needed \
    hyprland waybar swww dunst nwg-look \
    pamixer pavucontrol \
    thunar \
    wl-clipboard cliphist grim slurp wl-screenrec \
    fish vim neovim tmux tree-sitter-cli \
    fastfetch tree \
    tar zip unzip xdg-user-dirs \
    ttf-iosevka-nerd

```

```bash
# Install AUR packages
paru -S --needed tofi xcursor-pro-cursor-theme

```

```bash
# Set Fish default shell
echo $(which fish) | sudo tee -a /etc/shells
chsh -s $(which fish)

```

```bash
# Create user directories
xdg-user-dirs-update

```

```bash
# Clone repo & clean configs
git clone https://github.com/hananitallyson/i64dotfiles.git ~/i64dotfiles

rm -rf ~/.config/fastfetch \
       ~/.config/fish \
       ~/.config/hypr \
       ~/.config/imv \
       ~/.config/kitty \
       ~/.config/mako \
       ~/.config/mpv \
       ~/.config/nvim \
       ~/.config/tofi \
       ~/.config/waybar
```

```bash
# Create dotfile symlinks
ln -s ~/i64dotfiles/fastfetch          ~/.config/fastfetch
ln -s ~/i64dotfiles/fish               ~/.config/fish
ln -s ~/i64dotfiles/hypr               ~/.config/hypr
ln -s ~/i64dotfiles/kitty              ~/.config/kitty
ln -s ~/i64dotfiles/dunst              ~/.config/dunst
ln -s ~/i64dotfiles/nvim               ~/.config/nvim
ln -s ~/i64dotfiles/tofi               ~/.config/tofi
ln -s ~/i64dotfiles/waybar             ~/.config/waybar

```

```bash
# Set Git name & email
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

```

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your_email@example.com"

```

```bash
# Start SSH agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

```

```bash
# Show public key
cat ~/.ssh/id_ed25519.pub

```

```bash
# Test GitHub connection
ssh -T git@github.com

```
