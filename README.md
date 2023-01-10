# Ansible
Some ansible files for setting up a mac

## Running
1. install homebrew `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)`
2. install ansible `brew install ansible`
3. install ansible's community collection `ansible-galaxy collection install community.general`
4. run the playbook `ansible-pull -U https://github.com/Pearcekieser/ansible.git`

## References
- [fonts](https://github.com/fubarhouse/ansible-role-macfonts/blob/master/tasks/fonts.yml)
- **settings**
  - use `defaults read` and `defaults -currentHost read` to get current settings
  - diff settings with `diff a b` context can be included with `-U5`
  - use `defaults read-type` to get the type of a setting