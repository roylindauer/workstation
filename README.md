# Workstation

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

## Future things

Configure macos - 

```shell
tmutil addexclusion ~/Library/Containers/com.docker.docker
```

## Misc. 

I was running into an issue running `homebrew_cask` due to this bug - https://github.com/ansible-collections/community.general/issues/6842 

The version of brew installed returns a version number like ">=2.5.0" which is not a valid version number and causes the task to fail.

The solution was to actually remove `become: yes` from the task so that it used the local brew install instead of the one installed by Ansible. Seems weird. 

