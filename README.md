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
```
sh ~/Projects/dotfiles/symlinks/create-symlink-polybar.sh
```
14. Install yay
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
echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
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

16.install exa
```
yay -S exa
echo alias ls="exa --icons" >> ~/.zshrc
```
17. Install asdf
```
yay -S asdf-vm
echo source /opt/asdf-vm/asdf.sh >> ~/.zshrc
```

18. install languages
node
```
asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
asdf install nodejs 18.1.0
asdf global nodejs 18.1.0
npm install -g yarn
```

python
```
asdf plugin-add python
asdf install python 3.10.4
asdf global python 3.10.4
```
ruby
```
asdf plugin add ruby https://github.com/asdf-vm/asdf-ruby.git
asdf install ruby 3.1.2
asdf global ruby 3.1.2
```

go
```
asdf plugin-add golang https://github.com/kennyp/asdf-golang.git
asdf install golang 1.18.1
asdf global golang 1.18.1
```

rust
```
asdf plugin-add rust https://github.com/code-lever/asdf-rust.git
asdf install rust 1.60.0
asdf global rust 1.60.0
```

perl
```
asdf plugin-add perl
asdf install perl 5.35.11
asdf global perl 5.35.11
```

19. Install social work
```
yay -S slack-wayland zoom
```

20. add nvim
```
yay -S neovim
yay -S xsel
pip install pynvim
npm i -g neovim
cpanm -n Neovim::Ext
cpanm -n App::cpanminus
gem install neovim
sh ~/Projects/dotfiles/syslinks/create-sylink-nvim.sh
```
open nvim
exec :PackerSync

