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
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

5. Make a dir named 'Project' and clone your dotfiles in this dir
```
mkdir ~/Project
cd ~/Projects
git clone [dotfiles]
```
