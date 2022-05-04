# manjaro-for-dev
This is my config for initial dev in manjaro

1. Install Manjaro xfce
2. Update configs
`sudo pacman -Syyuu`
3. install base programs
- firefox
- vim
- git
4. Generate ssh and add to github
In terminal:
```
ssh-keygen -t ed25519 -C "your_email@example.com"
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

In github: add the ssh in your github

5. Make a dir named 'Project' and clone your dotfiles in this dir
```
mkdir ~/Project
cd ~/Projects
git clone [dotfiles]
```
6. install i3wm
` sudo pacman -S i3-wm i3status dmenu i3gaps`
7. Logout and enter in i3wm system
8. Get your i3 config
```sh ~/Projects/dotfiles/syslinks/create-symlink-i3.sh```
or copy the config

9. Get your X configs
```sh ~/Projects/dotfiles/syslinks/create-symlink-xconfig.sh```
or copy the config

(Now you have your powerfull keyboard!!!! Let's go!)

10. Instal more things
- polybar
- picom
- rofi
- kitty (or alacritty)

11. Get your kitty config
12. Get polybar config
13. Install yay
```
cd /tmp
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

14.Install zsh
```
yay -S zsh
chsh -s /usr/bin/zsh
```
15. Install powerlevel 10k and fonts
```
yay -S zsh-theme-powerlevel10k-git
yay -S ttf-meslo-nerd-font-powerlevel10k powerline-fonts awesome-terminal-fonts
```
exit and open terminal
options:
- y
- y
- y
- y
- 3(rainbow)
- unicode(1)
- 24-hour format(2)
- Angled(1)
- sharp(1)
- tail(1)
- Two lines(2)
- dotted(2)
- left(2)
- dark(3)
- compact(1)
- many icons(2)
- concise(1)
- y
- 1
- y
