# Configure Windows Subsystem for Linux

## Fedora 42

### Set up steps:
1) Install with `wsl --install FedoraLinux-42`
2) Install utils `sudo dnf install --allowerasing git zsh curl vim-default-editor`
3) Install oh-my-zsh `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
4) Update with `sudo dnf update`
5) Restart `wsl --shutdown`

## openSUSE Tumbleweed

### Set up steps:
1) Install with `wsl --install openSUSE-Tumbleweed`
2) Install utils `sudo zypper install git vim zsh curl system-group-wheel`
3) Add current user to wheel group `sudo usermod -aG wheel $USER`
4) Set visudo `sudo visudo` to allow wheel group without password and comment root password. Might need to close terminal, and open again.
5) Remove user password `sudo passwd -d $USER`
6) Remove root password `sudo passwd -d root`
7) Close session
8) Install oh-my-zsh `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
9) Update with `sudo zypper dup`
10) Restart `wsl --shutdown`
11) (Optional) Enable systemd `sudo zypper in -t pattern wsl_systemd`

## Azure Linux

Install guide here: wslazurelinux

### Set up steps:
1) Install utils `sudo tdnf install git curl vim`
2) Add current user to wheel group `sudo usermod -aG wheel $USER`
3) Set visudo `sudo visudo` to allow wheel group without password and comment root password. Might need to close terminal, and open again.
4) Remove user password `sudo passwd -d $USER`
5) Remove root password `sudo passwd -d root`
6) Close session
7) Update with `sudo tdnf -y upgrade`
8) Restart `wsl --shutdown`
