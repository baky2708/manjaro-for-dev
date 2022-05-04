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
` sudo pacman -S i3-wm i3status`
