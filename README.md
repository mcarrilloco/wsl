# Configuration for work Windows Subsystem for Linux
## openSUSE Tumbleweed

Set up steps:

1) Install utils `sudo zypper install git vim zsh curl system-group-wheel`
2) Add current user to wheel group `sudo usermod -aG wheel $USER`
3) Set visudo `sudo visudo` to allow wheel group without password and comment root password. Might need to close terminal, and open again.
4) Remove user password `sudo passwd -d $USER`
5) Remove root password `sudo passwd -d root`
6) Install oh-my-zsh `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
7) Update with `sudo zypper update`
