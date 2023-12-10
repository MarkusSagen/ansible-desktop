# ansible-desktop

## Pre-requisites

1. If on Mac, install Homebrew and Ansible 

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew install ansible
```

3. Install packages for your distro with:  
  
  
  Mac:
  ```sh 
  # TODO: might not work if having multiple files  
  ansible-pull -U https://github.com/MarkusSagen/ansible-desktop.git   
  ```

3. Or clone the repo and do the installation manually:
  
  ```sh
  ansible-playbook -i inventory playbooks/homebrew.yml

  # To install specific target and tasks
  ansible-playbook playbooks/homebrew.yml --limit=my.laptop --tags=packages
  ```

---

## Setting up the script

The instructions and inspiration for this is taken from: 
- https://opensource.com/article/22/6/install-software-macos-ansible-homebrew
- https://github.com/ruanbekker/ansible-macbook-setup

1. Install ansible 
  
  ```sh
  # pip install ansible==4.9.0
  brew install ansible  
  ```

2. Run this in your terminal

  ```sh
  cat << EOF >> inventory
  [localhost\]
  your-host-name
  EOF
  ```

3. Create a ansible playbook
