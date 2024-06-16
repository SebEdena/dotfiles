# My terminal configuration
This is my re-usable configuration for ZSH terminals.

Credits to the awesome videos of [@dreamsofautonomy](https://www.youtube.com/@dreamsofautonomy).

## Setup

This has been tested on `Debian`, `Ubuntu` and `MacOS`.

_Please do not clone immediately, wait for the instruction to do so._

### Install dependencies

```bash
# If Debian / Ubuntu
sudo sh -c 'apt update; apt upgrade -y'
apt install -y zsh git curl stow

# If MacOS
sh -c 'brew update; brew upgrade -y'
brew install -y zsh git curl stow
```

### Install `fzf`

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.local/share/fzf
~/.local/share/fzf/install --bin
```

### Install `zoxide`
```bash
curl -sS https://raw.githubusercontent.com/ajeetdsouza/zoxide/main/install.sh | zsh
```

### Clone `dotfiles` and create symlinks

```bash
git clone https://github.com/SebEdena/dotfiles ~/dotfiles
cd ~/dotfiles
stow .
```

### (Re)start ZSH
```bash
# If Debian / Ubuntu
chsh $USER -s /bin/zsh
exec zsh

# If MacOS
source ~/.zshrcc
```
