# Workstation

My workstation setup. I use Ansible to install applications and configure my dotfiles, which is in another repo at https://github.com/roylindauer/dotfiles 

## Setup

- Install Ansible
  ```shell
  python3 -m pip install --user ansible
  ```

- Install Ansible Requirements
  ```shell
  ansible-galaxy install -r requirements.yml
  ```

- Run Ansible Playbook
  ```shell
  ansible-playbook setup.yml
  ```

## Future Things

Configure macos - 

```shell
tmutil addexclusion ~/Library/Containers/com.docker.docker
```

