# Ansible
Some ansible files for setting up a mac

## Todo
- [ ] setup sub repo for `.dotfiles` and add ansible instructions for cloning and gnu-stow for the copying the files
  - install zsh `.zshrc` + oh-my-zsh (save zsh config) + powerlevel10k `.p10k.zsh`
  - global `.gitignore`
  - nvim config `~/.config/nvim/`
  - `~/.ideavimrc`
  - [ ] setup relative numbers for vscode 
- [ ] ? setup ansible for ssh keys - allows you to keep .dotfiles private 
- [ ] add custom zshrc for work
- [ ] learning tmux
  - [ ] add tmux installation
  - Server < session < window < pane 
  - common commands
    - `tmux a` -> reattach to prev session
    - prefix key `C-b` -> tells tmux that tmux server needs to do something (tmux server in a command mode `C-b d` to exit)
    - `tmux list-sessions`
    - `tmux new-session -d` creates a new detached session
    - `C-d [` 
- [ ] learning vim 

## Running
1. install homebrew `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)`
2. install ansible `brew install ansible`
3. install ansible's community collection `ansible-galaxy collection install community.general`
4. run the playbook `ansible-pull -U https://github.com/Pearcekieser/ansible.git`
5. log out and back in to apply settings changes 

## Troubleshooting
- use `ansible-pull -vvv` for verbose output
- `defaults could not write ...` -> make sure you are running in standard terminal and not iterm2

## References
- [fonts](https://github.com/fubarhouse/ansible-role-macfonts/blob/master/tasks/fonts.yml)
- **settings**
  - use `defaults read` and `defaults -currentHost read` to get current settings
  - diff settings with `diff a b` context can be included with `-U5`
  - use `defaults read-type` to get the type of a setting
- [dock](https://github.com/geerlingguy/ansible-collection-mac/blob/master/roles/dock/README.md)
- [mac settings](https://github.com/pawelgrzybek/dotfiles/blob/master/setup-macos.sh)